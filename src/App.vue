<template>
  <div id="app">
    <div class="ui fixed inverted menu vue-color">
    <div class="ui container">
      <a href="#" class="header item">Vue JS CRUD with Laravel API</a>
    </div>
    </div>
    <div class="ui main container">
      <Myform/>
      <CustomerList :customers="customers" />
    </div>
  </div>
</template>

<script>

import axios from "axios";
import Myform from "./components/Myform";
import CustomerList from "./components/CustomerList";
export default {
  name: 'App',
  components: {
    Myform,
    CustomerList
  },
  data() {
    return{
      url:"http://localhost/phpmyadmin/sql.php?server=1&db=laravel_api&table=customer&pos=0",
      customer:[]
    };
  },
  methods:{
    getCustomers(){
      axios.get(this.url).then(data=>{
        this.customers= data.data;
      });
    }
  },
  created(){
    this.getCustomers();
  }
};
</script>

<style>
.vue-color{
  background:#41b883 !important;
}

.main.container{
  margin-top:58px !important;
 
}

.submit-button{
  margin-top: 24px !important;
  float:right;
}
</style>
