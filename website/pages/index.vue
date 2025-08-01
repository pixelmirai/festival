<script setup lang="js">
import axios from "axios"



import { useWindowSize } from "@/composables/useWindowSize"
import { useInView } from "@/composables/useInView"
import { useScrollHandler } from "@/composables/useScrollHandler"
import GalleryMobile from "~/components/Section/GalleryMobile.vue";



const slider = ref(null)
const hero = ref(null);
const posts = ref([])


const program = ref(null)
const partners = ref(null);
const programClicked = ref(false)

function handleProgramButtonClick(){
  programClicked.value = true;
  scrollToSectionWithOffset(partners.value,-50)
}



function scrollToSectionWithOffset(element, offset = 0) {
  const section = element;
  if (section) {
    const rect = section.getBoundingClientRect();
    const scrollPosition = window.scrollY + rect.top + offset;

    window.scrollTo({
      top: scrollPosition,

    });
  }
}

onMounted(async () => {

})
</script>

<template>
  <div class="overflow-x-clip">
    <header class="fixed  top-0 h-[3rem] w-full   bg-[rgba(9,9,9,0.3) z-[999] ">
      <div class="w-full h-full flex justify-center md:justify-end items-center">
        <div class="flex gap-1  ">

            <button @click="handleProgramButtonClick" class="bg-black text-white px-2 py-1 font-extrabold rounded-sm    uppercase  ">
              <span>programma</span>
            </button>


          <a href="https://www.earlymusic.lv">
            <div class="bg-black text-white px-2 py-1 font-extrabold rounded-sm   uppercase  ">
              <span>kontakti</span>
            </div>
          </a>

          <a href="https://www.earlymusic.lv">
            <div class="bg-black text-white px-2 py-1 font-extrabold rounded-sm    uppercase  ">
              <span>earlymusic</span>
            </div>
          </a>
        </div>
      </div>
    </header>
    <main>

    </main>

    <div class=" background-video fixed z-[-20] top-0 w-screen h-screen overflow-hidden  bg-black">
      <video autoplay muted loop playsinline preload="none"  class="w-full h-full object-cover " src="assets/videos/remf-3.webm"></video>
    </div>

    <section class="relative  w-screen  h-[100dvh]  ">
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


    <section class=" w-full  ">
      <SectionDescription/>
    </section>

  <section>
    <SectionDescription2/>

  </section>


    <section>
        <SectionGallery2 class="hidden md:block"/>
        <GalleryMobile class="md:hidden block"/>
    </section>
    <section ref="partners" class="  ">
      <SectionPartners/>
    </section>

    <section id="program" ref="program" class="  ">
        <SectionProgram/>
    </section>

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