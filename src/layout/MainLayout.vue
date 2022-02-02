<template>
  <div class="wrapper">
      <div class="header-top">
          <logo/>
      </div>
      
      <router-view />
  </div>
</template>

<script>

import Logo from "../components/Logo.vue"
export default {
    name: 'MainLayout',
    components:{
        Logo
    }
}
</script>

<style lang="scss" scoped>

</style>