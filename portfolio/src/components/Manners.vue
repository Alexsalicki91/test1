<template>
  <div id="manners is-loaded">

		<!-- the router outlet, where all matched components would ber viewed -->
		<nav class="back-nav">
	  <div class="back">
			<router-link v-bind:to="'/'" style="font-size:15px ; color:#fff">Back</router-link>
		</div>
	</nav>
		<section class="section-project">
		<div class="section__bg">UI Application</div>
		<div class="section__project">
			<h2 class="section__title_project">Theatres Parisiens</h2>
			<div class="stripes-horizontal_project"></div>
		</div>
		<div class="section__info_launch">
			<p class="section__description_work">UI & UX Design
				<span class="section__description-inner"></span></p>
			</div>
		<div class="section__info_work">
			<p class="section__description_work">Work
				<span class="section__description-inner">UI Application</span></p>
			</div>
			<div class="section__info_client">
				<p class="section__description_work">Client
					<span class="section__description-inner">Theatresparisiensassocies.com</span></p>
				</div>
				<div class="section__info_project">ABOUT THE<br>PROJECT
					</div>
					<div class="section__description_project">I designed an Application for a client " Theatresparisiensassocies.com". With this application , we can see events in all theaters in Paris , see all informations that we search and we can buy tickets. So I worked on UI Design on more 30 screens's application.
						</div>
	</section>
	<section class="section-content-project-1">
		<div class="section__img-project">
				<img src="/static/theatre-section-1.gif">
			</div>
		</section>
		<section class="section-content-project-2">
			<div class="section__img-project">
				<img src="/static/theatre-section-2.gif">
			</div>
			</section>
			<section class="section-content-project-2">
				<div class="section__img-project">
					<img src="/static/theatre-section-3.gif">
				</div>
				</section>
				<section class="section-content-project-2">
					<div class="section__img-project">
						<img src="/static/theatre-section-4.gif">
					</div>
					</section>
					<section class="section-content-project-2">
						<div class="section__img-project">
							<img src="/static/theatre-section-5.gif">
						</div>
						</section>
				<section class="section-content-project-5">
					<div class="Next_project">
						<router-link v-bind:to="'/projects/adventure-wildlife'" style="font-size:70px ; color:#fff; margin-bottom:auto; margin-top:auto;">Next</router-link>
					</div>
					<div class="Info_project">Project
					<div class="Info_project_name">Adventure & Wildlife</div>
					</div>
				</section>
  </div>
</template>

<script>
export default {
  name: 'theatresparisiens',
	mounted() {



		// init controller
		(function () { // wait for document ready
			// init
			var controller = new ScrollMagic.Controller();

			// get all slides
			var slides = document.querySelectorAll(".section-content-project");

			// create scene for every slide
			for (var i=0; i<slides.length; i++) {
				new ScrollMagic.Scene({
						triggerElement: slides[i]
					})
					.setPin(slides[i])
          .removeIndicators()
					.addTo(controller);
			}
		});

		// init controller
		var controller = new ScrollMagic.Controller();

		// build scene


							new ScrollMagic.Scene({triggerElement: ".section-content-project-1"})
										.setTween(".section-project", {x: "", y:"-25%", ease: Linear.easeNone})
                    .removeIndicators()

										.addTo(controller);

										new ScrollMagic.Scene({triggerElement: ".section-content-project-2"})
													.setTween(".section-content-project-1", {x: "", y:"-10%", ease: Linear.easeNone})
													.removeIndicators()

													.addTo(controller);
													new ScrollMagic.Scene({triggerElement: ".section-content-project-1"})
																.setTween(".section__bg", {x: "-40%", y:"", ease: Linear.easeNone})
                                .removeIndicators()

																.addTo(controller);

									new ScrollMagic.Scene({triggerElement: ".section-content-project-3"})
										.setTween(".section-content-project-2", {x: "", y:"-25%", ease: Linear.easeNone})
										.removeIndicators()

										.addTo(controller);
										new ScrollMagic.Scene({triggerElement: ".section-content-project-4"})
											.setTween(".section-content-project-3", {x: "", y:"-25%", ease: Linear.easeNone})
                       .removeIndicators()

											.addTo(controller);

											var manners_vid = document.getElementById('manners-vid');

											var controller = new ScrollMagic.Controller();

											// build scene
											var scene = new ScrollMagic.Scene({triggerElement: ".section-content-project-3"})
															.addTo(controller)
															.removeIndicators()

															.on("enter", function () {
																manners_vid.play();
															})
															.on("leave", function () {
																manners_vid.currentTime=0;
																manners_vid.pause();
															})

															var manners_vid_2 = document.getElementById('manners-vid_2');

															var controller = new ScrollMagic.Controller();

															// build scene
															var scene = new ScrollMagic.Scene({triggerElement: ".section-content-project-4"})
																			.addTo(controller)
																			.removeIndicators()

																			.on("enter", function () {
																				manners_vid_2.play();
																			})
																			.on("leave", function () {
																				manners_vid_2.currentTime=0;
																				manners_vid_2.pause();
																			})





											imagesLoaded(document.querySelectorAll('#app'), () => {
												document.body.classList.remove('loading');
												// Init

											});

			var manners = new TimelineLite();

			manners
			.from($('.section__info_launch'), 0.5, { x:-10, autoAlpha: 0, ease:Power0.easeNone}, '1.5')
			.from($('.section__info_work'), 0.5, { x:-10,  autoAlpha: 0, ease:Power0.easeNone}, '1.5')
			.from($('.section__info_client'), 0.5, {x:-10,  autoAlpha: 0, ease:Power0.easeNone}, '1.5')
			.from($('.section__info_project'), 0.5, { x:-10, autoAlpha: 0, ease:Power0.easeNone}, '1.5')
			.from($('.section__description_project'), 0.6, { x:-10, autoAlpha: 0, ease:Power0.easeNone}, '1.5')
			.from($('.section__bg'), 0.3, { x:-50, autoAlpha: 0, ease:Power0.easeNone}, '2.5')
			.to($('.project'), 0.3, {  autoAlpha: 0, ease:Power0.easeNone}, '1')
			.from($('.back'), 0.3, {  autoAlpha: 0, ease:Power0.easeNone}, '2')


	}





}

</script>
<!-- styling for the component -->
<style>

@import "https://cdn.jsdelivr.net/npm/animate.css@3.5.1";



.section__project {
	animation-delay: 1s;
}

.pause-animation{
	animation-play-state: paused;
}



</style>
