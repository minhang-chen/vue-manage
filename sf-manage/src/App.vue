<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style>
    @import "./css/normalize.css";
    @import "./css/common.css";
    
    #app,body,html{
      font-family:"Microsoft YaHei";
      height: 100%;
      width: 100%;
      background:#f6f7fb;
    }

</style>
