<template>
  <div class="dropdown-container">
    <span class="dropdown-label">{{ label }}</span>
    <div class="dropdown">
      <div v-for="item in items" :key="item.value" class="dropdown-item">{{ item.label }}</div>
    </div>
  </div>
</template>

<script>
import '../assets/styles/dropdown-label.css'
export default {
  name: 'DropdownLabel',
  props: {
    label: {
      type: String,
      required: true
    },
    items: {
      type: Array,
      required: true,
      default: () => []
    }
  },
  data() {
    return {
      selectedLabel: ''
    }
  }
}
</script>
