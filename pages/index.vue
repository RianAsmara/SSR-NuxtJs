<template>
<div>
  <h1>Search iTunes</h1>
<br/>
<form @submit.prevent="submit">
  <input type="text" v-model="search" placeholder="Enter Artist Name" 
  autofocus >
</form>
</div>
</template>

<script>
export default {
  components: {

  },
  data() {
    return {
      search: ''
    }
  },
  methods: {
    submit(event) {
      this.$router.push(`results/${this.search}`);
    }
  }
}
</script>

<style>
* {
  text-align: center;
}
h1 {
  padding: 20px;
}
</style>
