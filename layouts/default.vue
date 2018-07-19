<template>
  <div>
    <TheHeader @sidenavToggle="dispalySidenav = !displaySidenav"/>
    <TheSidenav :show="dispalySidenav"
    @close="dispalySidenav = false"/>
      <nuxt/>
  </div>
</template>
<script>
import TheHeader from '@/components/Navigation/TheHeader'
import TheSidenav from '@/components/Navigation/TheSidenav'
export default {
  components: {
    TheSidenav,
    TheHeader
  },
  data(){
    return {
      dispalySidenav: false
    }
  }
}
</script>

<style>
html {
  font-family: 'Open Sans', sans-serif;
}
body {
  margin: 0;
}
</style>
