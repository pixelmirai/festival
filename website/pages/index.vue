<script setup lang="js">
import axios from "axios"



import { useWindowSize } from "@/composables/useWindowSize"
import { useInView } from "@/composables/useInView"
import { useScrollHandler } from "@/composables/useScrollHandler"
import ButtonProgramm from "~/components/ButtonProgramm.vue";


const slider = ref(null)
const hero = ref(null);
const posts = ref([])

function handleVideoLoaded(){
  console.log("video loaded")
  if (hero.value){
    hero.value.animate();
  }
}

onMounted(async () => {
 // hero.value.animate();
})
</script>

<template>
  <div class="">

    <div class=" background-video fixed z-[-20] top-0 w-screen h-screen overflow-hidden  bg-black">
      <video autoplay muted loop playsinline preload="none"  class="w-full h-full object-cover " src="assets/videos/herovideo-2.webm"></video>
    </div>





    <section class="relative  w-screen h-screen  min-h-[500px] lg:min-h-[800px] ">
     <SectionHero ref="hero"/>
      <div class="fixed w-full flex justify-center items-center bottom-4  ">
        <ButtonProgramm class="" />
      </div>

    </section>






    <div class=" w-full h-96 ">
      aaaaaaa
    </div>
    <div class="  w-screen h-96 ">
      aaaaaaa
    </div>
    <div class=" w-screen h-96 ">
      aaaaaaa
    </div>

  </div>
</template>
<style>

</style>