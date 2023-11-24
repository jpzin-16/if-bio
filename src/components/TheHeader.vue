<template>
    <div>
      <div class="container"></div>
      <span></span>
      <div class="nav">
        <a href="#">Página Inicial</a>
        <a href="#">Materiais</a>
        <a href="#">Encontros</a>
        <a href="#">Sobre nós</a>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'TheHeader',
    components: {},
  }
  </script>
  
  <style>
  .container {
    width: 100%;
    height: 157px;
    background-color: #2AA000;
  }
  
  .nav {
    background-color: #174F03;
    overflow: hidden;
  }
  
  .nav a {
    color: #fff;
    text-decoration: none;
    float: left;
    padding: 14px 16px;
    text-align: center;
    margin-right: 5px;
  }
  
  .nav a:hover {
    background-color: #3bbf48;
  }
  </style>
  