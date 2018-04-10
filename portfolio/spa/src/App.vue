<template>
  <div id="app">
		<div class="Grid">
			<div class="Grid-cell u-size12 u-offset2">
				<div class="Stripes-container">
					<div class="Stripes-item"></div>
				</div>
			</div>

		</div>
		<div class = "horizontal">
			<div class="stripes-horizontal_1"></div>
			<div class="stripes-horizontal_2"></div>
			<div class="stripes-horizontal_3"></div>
			<div class="stripes-horizontal_4"></div>
			<div class="stripes-horizontal_5"></div>
			<div class="stripes-horizontal_6"></div>

			<nav class="nav-top">
			<!-- the router outlet, where all matched components would ber viewed -->
			<router-link v-bind:to="'/'" style="padding:10px ; font-size:12px">+Projects</router-link>
			<router-link v-bind:to="'/about'"style="padding:10px ; font-size:12px">About</router-link>
			</nav>
			<nav class="network">
			<!-- the router outlet, where all matched components would ber viewed -->
			<router-link v-bind:to="'/'" style="padding:10px ; font-size:12px">Dribbble</router-link>
			<router-link v-bind:to="'/about'"style="padding:10px ; font-size:12px">Linkedin</router-link>
			</nav>
			<nav class="logo">
			<!-- the router outlet, where all matched components would ber viewed -->
			<router-link v-bind:to="'/'" style="padding:10px ; font-size:17px">Alex S.</router-link>
			</nav>
	</div>

  <transition name="router-anim">
    <router-view></router-view>
  </transition>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>


<!-- styling for the component -->
<style>

@import "https://cdn.jsdelivr.net/npm/animate.css@3.5.1";


.router-anim-enter-active {
	animation: coming 1s;
  animation-delay: .5s;
	opacity: 0;
}

.router-anim-leave-active {
	animation: going 1s;

}

@keyframes going {
	from {
		transform: translateX(0);
	}
	to {
		transform: translateX(-50px);
		opacity:0;
	}
}

@keyframes coming {
	from {
		transform: translateX(-50px);
		opacity: 0;
	}
	to {
		transform: translateX(0px);
		opacity: 1;
	}
}


</style>
