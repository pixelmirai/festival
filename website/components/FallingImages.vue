<script setup lang="js">
import {useInView} from "~/composables/useInView.js";

import {useUtils} from "~/composables/useUtils";

const images = ref(null)
const imagesInView = ref(false)
onMounted(()=>{

  if(images.value){
    useInView(images.value,()=>{
      imagesInView.value = true;
      console.log("in")
    },0)
  }



})
</script>

<template>
  <div ref="images"
       class="relative w-[300px]  " style="aspect-ratio: 10/16">
    <img src="assets/images/elina-simkus.jpg" alt=""
         :class="imagesInView ? 'image-1' : 'opacity-0'"
         class="absolute w-full h-full object-cover ">
    <img src="assets/images/monta-martinsone.jpg" alt=""
         :class="imagesInView ? 'image-2' : 'opacity-0'"
         class="absolute w-full h-full object-cover  ">
    <img src="assets/images/anete-viluma.jpg" alt=""
         :class="imagesInView ? 'image-3' : 'opacity-0'"
         class="absolute w-full h-full object-cover i">
    <img src="assets/images/anete-viluma.jpg" alt=""
         :class="imagesInView ? 'image-4' : 'opacity-0'"
         class="absolute w-full h-full object-cover i">
    <img src="assets/images/anete-viluma.jpg" alt=""
         :class="imagesInView ? 'image-5' : 'opacity-0'"
         class="absolute w-full h-full object-cover i z-20">
  </div>
</template>

<style scoped>
.image-1 {
  transform: translateX(-100rem) translateY(-100rem) rotateZ(0deg);
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
    transform: translateX(0) translateY(0) rotateZ(0deg);
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
    transform: translateX(-5rem) translateY(2rem) rotateZ(60deg);
  }
}

@keyframes insert-image-5 {
  from {
    transform: translateX(-100rem) translateY(-100rem) rotateZ(0deg);
  }
  to {
    transform: translateX(2rem) translateY(4rem) rotateZ(10deg);
  }
}


</style>