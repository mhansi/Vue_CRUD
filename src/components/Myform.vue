<template>
  <div class="my-form">
      <form class="ui form">
          <div class="fields">
              <div class="four wide field">
                  <label>First Name</label>
                  <input type="text" name="first_name"/>
              </div>

               <div class="four wide field">
                  <label>Last Name</label>
                  <input type="text" name="last_name"/>
              </div>

               <div class="four wide field">
                  <label>E-mail</label>
                  <input type="email" name="joe@gmail.com"/>
              </div>

              <div class="two wide field">
                  <button class="ui primary button submit-button">Save</button>
              </div>
          </div>
      </form>
  </div>
</template>

<script>
export default {
  name: "Myform"
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
