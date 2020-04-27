<template>
  <div id="app">
    <div class="ui fixed inverted menu vue-color">
    <div class="ui container">
      <a href="#" class="header item">Vue JS CRUD with Laravel API</a>
    </div>
    </div>
    <div class="ui main container">
      <Myform/>
    </div>
  </div>
</template>

<script>

import Myform from "./components/Myform";
export default {
  name: 'App',
  components: {
    Myform
  }
}
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
