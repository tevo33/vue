<template>
  <router-link class="router" :to="route">
    <span class="router-label">{{ label }}</span>
  </router-link>
</template>

<script>
import '../assets/styles/router-label.css'
export default {
  name: 'RouteLabel',
  props: {
    label: {
      type: String,
      required: true
    },
    route: {
      type: String,
      required: true
    }
  }
}
</script>
