<template>
  <div class="dropdown-container">
    <span class="dropdown-label">{{ label }}</span>
    <div class="dropdown">
      <div v-for="item in items" :key="item.value" class="dropdown-item">
        <RouteLabel :label="item.label" :route="item.route"></RouteLabel>
      </div>
    </div>
  </div>
</template>

<script>
import '../../../src/assets/styles/dropdown-label.css'
import RouteLabel from '../pageComponents/RouteLabel.vue'

export default {
  name: 'DropdownLabel',
  components: {
    RouteLabel
  },
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
