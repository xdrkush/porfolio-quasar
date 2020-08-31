<template>
  <div id='q-app' class="background">
    <router-view/>
  </div>
</template>
<script>
export default {
  name: 'App'
}
</script>
<style lang="scss">
.background {
  background: url('~assets/texture-polygone-multicolor.webp');
  background-size: cover;
  height: 100%;
  overflow: hidden;
}
</style>
