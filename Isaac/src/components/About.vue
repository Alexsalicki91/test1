<template>
  <div id="about">
		<section class="section-2">

		<div class="section__about">
			<h2 class="section__title_project">Hey, I'm Isaac Salehy</h2>
			<p class="section__description">Je suis actuellement en troisième année dans l’axe Animation 3D à l’Institut de l’internet et du Multimédia à la Défense. <br>Je suis passionné depuis longtemps par le cinéma d’animation, le multimédia ainsi que le jeu vidéo et je suis donc cette formation depuis 2016.
Ma licence dans l’axe Animation 3D m’apporte de solides compétences de modélisation et d’animation notamment grâce à la maitrise de différents logiciels (3Ds Max, Maya, Zbrush) mais également dans divers moteurs temps réels tels que Unity et Unreal Engine. <br>J’aime la modélisation et le texturing mais je préfère la gestion des projets.
Après avoir acquis des capacités techniques en 3D, je souhaite donc poursuivre mes études avec un mastère en Gestion de Production 3D. A long terme, je voudrais travailler dans le cinéma d’animation en tant que chargé de production.

				<span class="section__description-inner"><a href="/static/cv_isaac_salehy.pdf" download target=_blank style="padding:10px ; font-size:20px ; color:#fff; margin-top:auto; margin-bottom:auto ; text-decoration: underline;"><br>Download my CV
					</a></span></p>

		</div>


		<div class ="section__contact">
			<h1 class="section__title_contact">Personal Contact :</h1>
			<p class="section__description_contact">salehy.isaac@gmail.com<br>+33603208197
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
		<div class="loader-img">
			<img src=""/>
		</div>
		<div class="letter-a">A</div>
		<div class="letter-b">B</div>
		<div class="letter-o">O</div>
		<div class="letter-u">U</div>
		<div class="letter-t">T</div>
	</section>
  </div>
</template>

<script>
export default {
  name: 'about',
	mounted() {

		var about = new TimelineLite();

		about

		.from($('.letter-a'), 0.5, { autoAlpha: 0, ease:Power0.easeNone}, '2.5')
		.from($('.section__contact'), 0.5, { marginLeft:30, autoAlpha: 0, ease:Power0.easeNone}, '2')
		.from($('.section__description_about_me'), 0.5, { marginLeft:30, autoAlpha: 0, ease:Power0.easeNone}, '2')
		.from($('.section__title_project'), 0.5, { x:-30, autoAlpha: 0, ease:Power0.easeNone}, '1.5')
		.from($('.section__description'), 0.8, {  autoAlpha: 0, ease:Power2.easeIn}, '1.7')
		.from($('.letter-b'), 0.5, { autoAlpha: 0, ease:Power0.easeNone}, '3')
		.from($('.letter-o'), 0.5, { autoAlpha: 0, ease:Power0.easeNone}, '3.5')
		.from($('.letter-u'), 0.5, { autoAlpha: 0, ease:Power0.easeNone}, '4')
		.from($('.letter-t'), 0.5, { autoAlpha: 0, ease:Power0.easeNone}, '4.5')
		.to($('.project'), 0.3, {  autoAlpha: 5, ease:Power0.easeNone}, '1.5')



	}

}
</script>
<!-- styling for the component -->
<style>

@import "https://cdn.jsdelivr.net/npm/animate.css@3.5.1";


.section__about {
	animation-delay: 1.5s;
}

.pause-animation {
	animation-play-state: paused;
}

</style>
