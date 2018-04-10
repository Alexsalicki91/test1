<template>
  <div id="about">
		<section class="section-2">
    <transition :duration="1000" name="fade">
		<div class="section__about">
			<h2 class="section__title_about">Hey,</h2>
			<p class="section__description">Enim funeribus nemo ad has Scironis Scironis nemo quae quae ad pilatorum ut praerupta sed navem contigui quae navigabant deinde sunt contigui letalia letalia navem sed navigabant has appulit has.
				<span class="section__description-inner"></span></p>
		</div>
		</transition>


		<div class ="section__contact">
			<h1 class="section__title_contact">Personal Contact :</h1>
			<p class="section__description_contact">salicki.alex@gmail.com<br>+33632913360
				<span class="section__description-inner"></span></p>
		</div>


		<div class="section__info">
			<p class="section__description_info">Coded and Designed by Alex Salicki
				<span class="section__description-inner"></span></p>
		</div>
		<div class="section__about_me">
			<p class="section__description_about_me">About me
				<span class="section__description-inner"></span></p>
		</div>
		<div class="letter-a">A</div>
		<div class="letter-b">B</div>
		<div class="letter-o">O</div>
	</section>
  </div>
</template>

<script>
export default {
  name: 'about',

};
</script>
<!-- styling for the component -->
<style>

@import "https://cdn.jsdelivr.net/npm/animate.css@3.5.1";



	.fade-enter-active {
		animation: coming 1s;
	  animation-delay: .5s;
		opacity: 0;
	}

	.fade-leave-active {
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
