<template>
  <div class="header">
    <img src="/imgs/suprivita-header-logo.png" alt="header-logo" height="200px;" width="200px;" />
    <div class="options-div">
      <RouteLabel label="Nosso DNA" route="/" />
      <DropdownLabel label="O que fazemos" :items="dropdownItems" />
      <DropdownLabel label="Contato" :items="dropdownItems" />
      <RouteLabel label="Conteúdos" route="/" />
      <input class="search-input" type="text" v-model="input" placeholder="Pesquise..." />
    </div>
  </div>
</template>

<script>
import '../assets/styles/header.css'
import RouteLabel from '../components/RouteLabel.vue'
import DropdownLabel from './DropdownLabel.vue'

export default {
  name: 'HeaderComponent',
  components: {
    RouteLabel,
    DropdownLabel
  },
  data() {
    return {
      dropdownItems: [
        { value: '1', label: 'Item 1' },
        { value: '2', label: 'Item 2' },
        { value: '3', label: 'Item 3' }
      ]
    }
  }
}
</script>
