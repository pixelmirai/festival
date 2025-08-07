<script setup lang="js">
import axios from "axios"
import {useUtils} from "~/composables/useUtils.js";


const utils = useUtils();

/*



*
*



*
* description2 - figure out what is in description 2 image
*

*

*
* program -  add days and written adresses
* program decid better bottom padding
*
*
*partners find and insert correct logos
*
* ing colleg make window green
*
*
*
*
* */




const timg = ref("")

const slider = ref(null)
const hero = ref(null);
const posts = ref([])

const gallery = ref(null);
const program = ref(null)
const contact = ref(null);
const partners = ref(null);
const programClicked = ref(false)




function handleProgramButtonClick(){
  programClicked.value = true;
  scrollToSectionWithOffset(program.value,-50)
}

function handleContactButtonClick(){
  programClicked.value = true;
  scrollToSectionWithOffset(contact.value,-50)
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
const activeSections = ref({
  program: {
    element: program.value,
    vhr: 0,
    active: false,
  },
  contact: {
    element: contact.value,
    vhr: 0,
    active: false,
  },
});




onMounted(async () => {
  activeSections.value = {

    program: {
      element: program.value,
      vhr: 0,
      active: false,
    },
    contact: {
      element: contact.value,
      vhr: 0,
      active: false,
    },
  }
  console.log(activeSections.value.program.active)


  window.addEventListener('scroll',() => {

    const centerLine = window.innerHeight / 2

    activeSections.value.program.active =
        utils.isCentralElement(activeSections.value.program.element, 0.5)
    activeSections.value.contact.active =
        utils.isCentralElement(activeSections.value.contact.element, 0.5) ||
        utils.isCentralElement(partners.value, 0.5) ;


  })

})
</script>

<template>
  <div class="overflow-x-clip">
    <header class="fixed  top-0 h-[3rem] w-full px-4    bg-[rgba(9,9,9,0.3) z-[999] ">
      <div class="w-full h-full flex justify-center md:justify-end items-center">
        <div class="flex gap-1  ">

            <button
                :class="activeSections.program.active ? 'bg-white text-black border-2 border-black ':'bg-black text-white'"
                @click="handleProgramButtonClick" class="  hover:bg-white  border-2 border-black hover:text-black  px-2 py-1 font-extrabold rounded-sm    uppercase  ">
              <span>programma</span>
            </button>


            <button
                :class="activeSections.contact.active ? 'bg-white text-black':'bg-black text-white'"
                @click="handleContactButtonClick"
                class=" px-2 py-1 font-extrabold rounded-sm  hover:bg-white  border-2  border-black hover:text-black   uppercase  ">
              <span>kontakti</span>
            </button>


          <a href="https://www.earlymusic.lv">
            <div class="bg-black text-white px-2 py-1 font-extrabold rounded-sm  border-2  border-black   uppercase  ">
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
    <div>
      <img :src="timg" alt="">
    </div>

    <section class=" w-full  ">
      <SectionDescription/>
    </section>

  <section>
    <SectionDescription2/>
  </section>


    <section ref="gallery">
        <SectionGallery2 class="hidden md:block"/>
        <SectionGalleryMobile class="md:hidden block"/>
    </section>


    <section id="program" ref="program" class="  ">
        <SectionProgram/>
    </section>
    <section ref="partners" class="  ">
      <SectionPartners/>
    </section>

    <footer ref="contact" class=" ">

      <SectionContact/>
    </footer>
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