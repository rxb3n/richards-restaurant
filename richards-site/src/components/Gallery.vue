<template>
	<div class="gallery-container">
		<swiper
			:modules="modules"
			:space-between="0"
			:grabCursor = "true"
			:loop="true"
			:freeMode = "true"
			:speed ="10000"
			:freeModeMomentum = "true"
			:autoplay= "{
				delay: 1,
				disableOnInteraction: false
			}"
			:breakpoints="{
				'950': {
					slidesPerView: 3,
					spaceBetween: 0,
				},
				'0': {
					slidesPerView: 1,
					spaceBetween: 5,
				},
			}"
			@swiper="onSwiper"
			@slideChange="onSlideChange"
		>
			<swiper-slide class="gallery-img-container"
				><img
					class="gallery-img"
					src="../assets/thumbnail_image001.jpg"
					loading="lazy"
					alt="Intérieur accueillant du restaurant Canari"
			/></swiper-slide>
			<swiper-slide class="gallery-img-container"
				><img
					class="gallery-img"
					src="../assets/thumbnail_image003.jpg"
					loading="lazy"
					alt="Elegant dining au restaurant Canari"
			/></swiper-slide>
			<swiper-slide class="gallery-img-container"
				><img
					class="gallery-img"
					src="../assets/thumbnail_image002.jpg"
					loading="lazy"
					alt="Peinture trouvée à l'intérieur du restaurant Canari"
			/></swiper-slide>

			<swiper-slide class="gallery-img-container"
				><img
					class="gallery-img"
					src="../assets/thumbnail_image005.jpg"
					loading="lazy"
					alt="Peinture trouvée à l'intérieur du restaurant Canari"
			/></swiper-slide>

			
			<swiper-slide class="gallery-img-container"
				><img
					class="gallery-img"
					src="../assets/thumbnail_image006.jpg"
					loading="lazy"
					alt="Peinture trouvée à l'intérieur du restaurant Canari"
			/></swiper-slide>

			
			<swiper-slide class="gallery-img-container"
				><img
					class="gallery-img"
					src="../assets/thumbnail_image004.jpg"
					loading="lazy"
					alt="Peinture trouvée à l'intérieur du restaurant Canari"
			/></swiper-slide>

			...
		</swiper>
	</div>
</template>
<script>
// import Swiper core and required modules
import { Navigation, Pagination, Scrollbar, A11y, Autoplay } from "swiper/modules";

// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css/scrollbar";

// Import Swiper styles
export default {
	components: {
		Swiper,
		SwiperSlide,
	},
	setup() {
		const onSwiper = swiper => {
			console.log(swiper);
		};
		const onSlideChange = () => {
			console.log("slide change");
		};
		return {
			onSwiper,
			onSlideChange,
			modules: [Navigation, Pagination, Scrollbar, A11y, Autoplay],
		};
	},
};
</script>

<style scoped>
@import "../style.css";
</style>
