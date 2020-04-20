<template>
  <div id="app">
    <router-view name="blank" />
    <router-view />
  </div>
</template>

<style>
  html,body,#app {
    width: 100%;
    height: 100%;
    margin: 0 auto;
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    overflow: hidden;
  }
</style>

