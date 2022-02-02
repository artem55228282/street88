<template>
  <div id="app">
     <component :is="layout">
      <router-view></router-view>
    </component>
  </div>
</template>

<script>
import MainLayout from "./layout/MainLayout.vue"
export default{
  
   name: "App",
   components: {
     MainLayout
   },
    computed: {
    layout(){
      return (this.$route.meta.layout || 'empty') + '-layout';
    }
  }
}

</script>

<style lang="scss">


*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
a{
  text-decoration: none;
}
li{
  list-style: none;
}
.wrapper{
  width: 100%;
}
</style>
