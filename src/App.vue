<template>
  <HeaderComponent />
  <main>
    <router-view></router-view>
  </main>
</template>

<script>
import HeaderComponent from '../src/components/pageComponents/HeaderComponent.vue'
export default {
  name: 'App',
  components: {
    HeaderComponent
  }
}
</script>

<style lang="css"></style>
