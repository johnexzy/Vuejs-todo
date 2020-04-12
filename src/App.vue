<template>
  <div id="app">
    <!-- <img src="./assets/logo.png"> -->
    <!-- <nav>
    <router-link to="/">HOME</router-link>
    <router-link to="/about/John">ABOUT</router-link>  
    </nav>
    
    <router-view/> -->
    <HelloWorld/>
    
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'

export default {
  name: 'App',
  components:{
    HelloWorld
  }
}
</script>
<style>
body{
  background-color: #eeeeee;
  display: grid;
  grid-template-rows: auto;
  justify-items: center;
  align-items: center
}
body html{
  margin: 0;
  height: 100%;
}
#app{
  width: 50%
}
</style>
