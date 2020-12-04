<template>

  <div class="d-sm-none">
    <div style="float:left;"> 
      <Slide :closeOnNavigation="true">
        <div class="mobile-menu-link" v-on:click="navigate('home')">
          <vue-fontawesome icon="home" size="2" color="white"></vue-fontawesome>
          <span>HOME</span>
        </div>
        <br>
        <div class="mobile-menu-link" v-on:click="navigate('servizi')">
          <vue-fontawesome icon="wrench" size="2" color="white"></vue-fontawesome>
          <span>SERVIZI</span>
        </div>
        <br>
        <div class="mobile-menu-link" v-on:click="navigate('prenota')">
          <vue-fontawesome icon="clipboard" size="2" color="white"></vue-fontawesome>
          <span>PRENOTA</span>
        </div>
        <br>
        <div class="mobile-menu-link" v-on:click="navigate('dove-siamo')">
          <vue-fontawesome icon="globe" size="2" color="white"></vue-fontawesome>
          <span>DOVE SIAMO</span>
        </div>
        <br>
        <div class="mobile-menu-link" v-on:click="navigate('promozioni')">
          <vue-fontawesome icon="euro" size="2" color="white"></vue-fontawesome>
          <span>PROMOZIONI</span>
        </div>
      </Slide>
    </div>
    <div style="float:right;">
      <img src="../assets/header.png" class="img-top-banner-mobile">
    </div>
  </div>      

</template>

<script>
import { Slide } from 'vue-burger-menu'  // transition

export default {
  name: 'menuMobile',
  components: {
    Slide
  },
  methods: {
		navigate(page) {
			this.$root.$emit('navigate', page);
		}
	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.img-top-banner-mobile {
  max-width: 100%;
  height: auto;
}
.mobile-menu-link i{
  width: 20%;
  height: auto;
}
.mobile-menu-link span {
  margin-left: 5px;
}
</style>