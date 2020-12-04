<template>
  <div id="app" class="container-fluid">
    <topBanner/>
    <menuMobile/>
    <home v-if="this.page==='home'"/>
    <servizi v-if="this.page==='servizi'"/>
    <prenota v-if="this.page==='prenota'"/>
    <doveSiamo v-if="this.page==='dove-siamo'"/>
    <promozioni v-if="this.page==='promozioni'"/>
  </div>
</template>

<script>

import topBanner from './components/topBanner.vue'
import menuMobile from './components/menuMobile.vue'
import home from './components/home.vue'
import servizi from './components/servizi.vue'
import prenota from './components/prenota.vue'
import doveSiamo from './components/doveSiamo.vue'
import promozioni from './components/promozioni.vue'

export default {
  name: 'App',
  components: {
    topBanner,
    menuMobile,
    home,
    servizi,
    prenota,
    doveSiamo,
    promozioni
  },
  data: function() {
    return {
      page: 'home'
    }
  },
  mounted() {
		this.$root.$on('navigate',arg => {
      this.page = arg;
		});
	}
}
</script>

<style>
#app {
  font-family: "Noto Sans", sans-serif;
}
#app .bm-menu {
  z-index: 5;
  background-color: #161617;
}
#app .bm-burger-button {
  position: relative;
  left: 2%;
  top: 15px;
  height: 20px;
  width: 25px;
}
#app .bm-burger-bars {
  background-color: #c40606;
}
</style>
