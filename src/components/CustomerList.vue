<template>
  <div class="customer-list">
     <div class="data">
         <table class="ui celled table">
             <thead>
                 <tr>
                 <th style="width:50px; text-align: center;">#</th>
                 <th>Name</th>
                 <th>E-mail</th>
                 <th style="width:148px;">Action</th>
                 </tr>
             </thead>
             <tbody>
                 <Customer v-for="customer in customers" 
                           :key="customer.id"
                           :customer="customer"/>
             </tbody>
         </table>
     </div>
  </div>
</template>

<script>

import Customer from "./Customer"
export default {
  name: "CustomerList",
  components:{
      Customer
  },
  props: {
      customer:{
          type:Array
      }
  }
  
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
