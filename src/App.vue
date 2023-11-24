<template>
  <div>
    <TheHeader/>
    <TheHome/>  
    <TheAbout/>
    <TheContact/>
    <TheFooter/>
  </div>
</template>

<script>
import TheAbout from './components/TheAbout.vue';
import TheHeader from './components/TheHeader.vue';
import TheHome from './components/TheHome.vue';
import TheContact from './components/TheContact.vue';
import TheFooter from './components/TheFooter.vue';
  export default {
    name: "App",
    components: {
    TheHeader,
    TheHome,
    TheAbout,
    TheContact,
    TheFooter
},
    data(){return{}}
  }
</script>

<style>
  body{
    border: 0;
    padding: 0;
    margin: 0;
    overflow-x: hidden;
    overflow-y: scroll;
    font-family: Arial, Helvetica, sans-serif;
  }
</style>