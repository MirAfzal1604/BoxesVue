
<template>
<div class="main">
  <header-v></header-v>
  <main-v></main-v>
</div>
</template>

<script>
import header from "./components/header.vue"
import main from "./components/main.vue"

export default {
  name: 'App',
  
  components: {
    'header-v': header,
    'main-v': main,
},

  data() {
    return {
    
    }
  }
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
}
html,
body{
  height: 100vh;
}
h1,
h2,
h3,
h4,
h5,
h6 {
    margin-bottom: 0;
}

p {
    margin-bottom: 0;
}

ul {
    padding: 0;
    margin-bottom: 0rem;
}

li {
    list-style: none;
}

a {
    text-decoration: none;
}
.main{
  background-color: #055;
  width: 100%;
  height: 100%;
}
</style>