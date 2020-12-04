<template>
  <div class="topBanner">

    <div class="container-fluid d-none d-md-block" id="top-menu"> 
      <div class="row">
          <div class="col-md-1 col-lg-1 col-xl-1">
              &nbsp;
          </div>
          <div class="col-md-2 col-lg-2 col-xl-2">
              <span v-on:click="navigate('home')" class="menu-link">HOME</span>
          </div>
          <div class="col-md-2 col-lg-2 col-xl-2">
              <span v-on:click="navigate('servizi')" class="menu-link">SERVIZI</span>
          </div>
          <div class="col-md-2 col-lg-2 col-xl-2">
              <span v-on:click="navigate('prenota')" class="menu-link">PRENOTA</span>
          </div>
          <div class="col-md-2 col-lg-2 col-xl-2">
              <span v-on:click="navigate('dove-siamo')" class="menu-link">DOVE SIAMO</span>
          </div>
          <div class="col-md-2 col-lg-2 col-xl-2">
              <span v-on:click="navigate('promozioni')" class="menu-link">PROMOZIONI</span>
          </div>
          <div class="col-md-1 col-lg-1 col-xl-1">
              &nbsp;
          </div>
      </div>
      <div class="row">
        <div class="col-md-12 col-lg-12 col-xl-12">
            <img src="../assets/header.png" class="img-top-banner">
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'topBanner',
  methods: {
		navigate(page) {
			this.$root.$emit('navigate', page);
		}
	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.img-top-banner {
  max-width: 100%;
  height: auto;
}
#top-menu {
  padding-top: 1.5%;
  text-align: center;
  font-weight: bold;
  color: black;
  font-size: 110%;
}
.menu-link{
  font-family: "Noto Sans", sans-serif;
  color: black;
  font-weight: bold;
  font-size: 110%;
  text-decoration: none;
  transition: all 0.4s ease-out;
  cursor: pointer; 
}
.menu-link:hover {
  color: #c40606;
  transition: all 0.1s ease-out;
}
</style>
