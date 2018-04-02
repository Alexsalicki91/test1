<template>
  <div id="app">
		<nav class="demos">
  <!-- the router outlet, where all matched components would ber viewed -->
  <router-link v-bind:to="'/'">Home</router-link>
<router-link v-bind:to="'/about'">About</router-link>
</nav>
    <router-view></router-view>

  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>


<!-- styling for the component -->
<style>
#app {

}
</style>
