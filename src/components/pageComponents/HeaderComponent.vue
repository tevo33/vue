<template>
  <div class="header">
    <img src="/imgs/suprivita-header-logo.png" alt="header-logo" height="200px;" width="200px;" />
    <div class="options-div">
      <RouteLabel label="Nosso DNA" route="/" />
      <DropdownLabel label="O que fazemos" :items="whatWeDoItems" />
      <DropdownLabel label="Contato" :items="contactItems" />
      <RouteLabel label="Conteúdos" route="/" />
      <input class="search-input" type="text" v-model="input" placeholder="Pesquise..." />
    </div>
  </div>
</template>

<script>
import '../../../src/assets/styles/header.css'
import RouteLabel from '../pageComponents/RouteLabel.vue'
import DropdownLabel from '../pageComponents/DropdownLabel.vue'

export default {
  name: 'HeaderComponent',
  components: {
    RouteLabel,
    DropdownLabel
  },
  data() {
    return {
      whatWeDoItems: [
        { label: 'Qualidade', route: '/' },
        { label: 'Tecnologia', route: '/' },
        { label: 'Formas Farmacêuticas', route: '/' },
        { label: 'Injetáveis', route: '/' },
        { label: 'Homeopatias', route: '/' }
      ],
      contactItems: [
        { label: 'Intagram', route: '/' },
        { label: 'YouTube', route: '/' }
      ]
    }
  }
}
</script>
