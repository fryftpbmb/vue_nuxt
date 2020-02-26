<template>
  <div class="container">
    <p>{{users[0].id}},{{users[0].name}}</p>
    <hr>
    <router-link to="/price">PricePage</router-link>
  </div>
</template>

<script>
  const axios = require('axios')
  let url = 'https://jsonplaceholder.typicode.com/users'

  export default{
    asyncData({ params }){
      return axios.get(url).then((res)=>{
        return{users:res.data}
      })
    }
  }
</script>

<style>

</style>
