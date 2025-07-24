<script setup lang="js">
import axios from "axios"



import { useWindowSize } from "@/composables/useWindowSize"
import { useInView } from "@/composables/useInView"
import { useScrollHandler } from "@/composables/useScrollHandler"
import ButtonProgramm from "~/components/ButtonProgramm.vue";


const slider = ref(null)
const hero = ref(null);
const posts = ref([])


const program = ref(null)
const programClicked = ref(false)

function handleProgramButtonClick(){
  programClicked.value = true;
  scrollToSectionWithOffset(program.value,0)
}

function scrollToSectionWithOffset(element, offset = 0) {
  const section = element;
  if (section) {
    const rect = section.getBoundingClientRect();
    const scrollPosition = window.scrollY + rect.top + offset;

    window.scrollTo({
      top: scrollPosition,
      behavior: 'smooth'
    });
  }
}

function handleVideoLoaded(){

}

onMounted(async () => {
 // hero.value.animate();
})
</script>

<template>

  <div class="">


    <div class=" background-video fixed z-[-20] top-0 w-screen h-screen overflow-hidden  bg-black">
      <video autoplay muted loop playsinline preload="none"  class="w-full h-full object-cover " src="assets/videos/remf-3.webm"></video>
    </div>





    <section class="relative  w-screen  h-screen  ">
      <div class="absolute w-full h-full">
        <SectionHero class="absolute" ref="hero"/>
      </div>
      <div class="absolute flex items-end  w-full h-full">
        <div
            :class="{'opacity-0':programClicked}"
            class="button-space flex justify-center items-center w-full h-[8rem] ">
          <ButtonProgramm @click="handleProgramButtonClick" class="" />
        </div>
      </div>




    </section>






    <div class=" w-full  ">
      <SectionFirst2/>
    </div>
    <div ref="program" class="  w-screen h-96 ">

    </div>
    <div class=" w-screen h-96 ">
      aaaaaaa
    </div>

  </div>
</template>
<style>
.programButton{
  visibility: hidden;
  opacity: 0;
  animation: programButtonDissappear 1s linear forwards;
}
@keyframes programButtonDisappear{
  from {
    visibility: visible;
    opacity: 1;
  }to{
       visibility: hidden;
     opacity: 0;
   }
}
</style>