<script setup lang="js">
import {useInView} from "~/composables/useInView.js";

import {useUtils} from "~/composables/useUtils";

const IMG_URL = "https://rvmdfcontent.wordpress.com/wp-content/uploads/2025/08/"

const images = ref([
  `${IMG_URL}description-anete-viluma.webp`,
  `${IMG_URL}hero-maris-kupcs.webp`,
  `${IMG_URL}hero-elina-simkus.webp`,
  `${IMG_URL}hero-erik-bosgraf.webp`,
  `${IMG_URL}hero-monta-martinsone.webp`,
  `${IMG_URL}hero-anete-viluma.webp`,
  `${IMG_URL}hero-mauro.webp`,
  `${IMG_URL}maza-gilde-orchestra.webp`,
])



const imagesInView = ref(false)
onMounted(()=>{

  if(images.value){
    useInView(images.value,()=>{
      imagesInView.value = true ;
    },0.2)
  }



})
</script>

<template>
  <div ref="images"
       class="relative w-[256px] md:w-[260px]  " style="aspect-ratio: 10/16;
        border: solid 	#B0927A 20px;
        background-color: #374231;
">
    <div class="absolute w-full h-full flex  justify-center items-center">
      <img src="assets/images/keys.png" alt="" class="w-[8rem]">
    </div>
      <div v-if="imagesInView">
        <img src="assets/images/description/description-bosgraf.webp" alt=""
             :class="imagesInView ? 'image-1' : 'opacity-0'"
             class="absolute w-full h-full object-cover ">
        <img src="assets/images/description/description-jolanta-barinska.webp" alt=""
             :class="imagesInView ? 'image-2' : 'opacity-0'"
             class="absolute w-full h-full object-cover  ">
        <img src="assets/images/description/description-monta-martinsone.webp" alt=""
             :class="imagesInView ? 'image-3' : 'opacity-0'"
             class="absolute w-full h-full object-cover i">
        <img src="assets/images/description/description-anete-viluma.webp" alt=""
             :class="imagesInView ? 'image-4' : 'opacity-0'"
             class="absolute w-full h-full object-cover i">
        <img src="assets/images/description/description-elina-simkus.webp" alt=""
             :class="imagesInView ? 'image-5' : 'opacity-0'"
             class="absolute w-full h-full object-cover i z-20">
      </div>
    </div>


</template>

<style scoped>
.image-1 {
  transform: translateX(-60rem) translateY(-60rem) rotateZ(0deg);
  animation: insert-image-1 1s linear 0s forwards;
}

.image-2 {
  transform: translateX(-100rem) translateY(-100rem) rotateZ(0deg);
  animation: insert-image-2 1s linear 1s forwards;
}

.image-3 {
  transform: translateX(-100rem) translateY(-100rem) rotateZ(0deg);
  animation: insert-image-3 1s linear 2s forwards;
}

.image-4 {
  transform: translateX(-100rem) translateY(-100rem) rotateZ(0deg);
  animation: insert-image-4 1s linear 3s forwards;
}

.image-5 {
  transform: translateX(-100rem) translateY(-100rem) rotateZ(0deg);
  animation: insert-image-5 1s linear 4s forwards;
}


@keyframes insert-image-1 {
  from {
    transform: translateX(-100rem) translateY(-100rem) rotateZ(0deg);
  }
  to {
    transform: translateX(2rem) translateY(0) rotateZ(10deg);
  }
}

@keyframes insert-image-2 {
  from {
    transform: translateX(-100rem) translateY(-100rem) rotateZ(0deg);
  }
  to {
    transform: translateX(-1rem) translateY(-1rem) rotateZ(-2deg);
  }
}

@keyframes insert-image-3 {
  from {
    transform: translateX(-100rem) translateY(-100rem) rotateZ(0deg);
  }
  to {
    transform: translateX(-2rem) translateY(-2rem) rotateZ(-20deg);
  }
}

@keyframes insert-image-4 {
  from {
    transform: translateX(-100rem) translateY(-100rem) rotateZ(0deg);
  }
  to {
    transform: translateX(2rem) translateY(2rem) rotateZ(30deg);
  }
}

@keyframes insert-image-5 {
  from {
    transform: translateX(-100rem) translateY(-100rem) rotateZ(0deg);
  }
  to {
    transform: translateX(2rem) translateY(7rem) rotateZ(10deg);
  }
}


</style>