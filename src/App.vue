<template>
<mytable 
  v-bind:tdata="tdata"
/>
</template>

<script>

import mytable from '@/components/mytable'
export default {
  name: 'App',
  data() {
    
    
    return {

      tdata: [
       {id:-1, name: 'MacBook', artikul: '54f', category: 'notebook', weight: 1.2, ownprice: 300000, status: 'new', adddate: '06.02.2020'} 
      ]

    }
  },
  mounted() {
    // const urls = 'https://api.coindesk.com/v1/bpi/currentprice.json';
    const urls = 'http://127.0.0.1/example/public/name';
   fetch(urls, {mode: 'cors'})
  .then(function(response) {
    return response.text();
  })
  .then(function(text) {
    console.log('Request successful', text);
  })
  .catch(function(error) {
    log('Request failed', error)
  });
   /* console.log(response);*/
    

  
  },
  components: {
    mytable
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
