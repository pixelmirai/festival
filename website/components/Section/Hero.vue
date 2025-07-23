<script setup lang="js">
import {useUtils} from "~/composables/useUtils.js";


const utils = useUtils()


const heroSlider = ref(null);
const sliderInterval = ref(null)
const sliderIntervalCounter = ref(0)
defineExpose({
  animate
})

onMounted(()=>{
  animate()

  if(heroSlider.value){
    sliderInterval.value = window.setInterval(() => {
      if (heroSlider.value) {
        heroSlider.value.moveLeft(0.001)
        sliderIntervalCounter.value++
      }

      if (sliderIntervalCounter.value >= 500) {
        clearInterval(sliderInterval.value)
        sliderInterval.value = undefined
      }
    }, 20)
  }

})

const open = ref(false)
const fadeBlack = ref(false)
const firstBackground = ref(false)
const sliderFadeOut = ref(false)
function slideOpen(){

}

function animate(){
  setTimeout(()=>{
    fadeBlack.value = true
  },200)
  setTimeout(()=>{
    firstBackground.value = true
  },2000)
  setTimeout(()=>{
   sliderFadeOut.value = true;
  },3000)




}

</script>

<template>
  <div class="relative w-full h-full min-h-[500px] lg:min-h-[800px] ">

    <div
        :class="sliderFadeOut ? 'opacity-0':'opacity-90'"
        class="first-layer absolute flex w-full h-full overflow-hidden transition-opacity  ease-linear"
      style="transition-duration: 3s"
    >

      <HeroSlider ref="heroSlider" class=" ">

        <div class="h-[120vh] w-[32rem]">
          <img src="assets/images/maza-gilde-2.jpg" alt="" class="w-full h-full object-cover" >
        </div>
        <div class="h-screen w-[32rem]">
          <img src="assets/images/maza-gilde-orchestra.webp" alt="" class="w-full h-full object-cover">
        </div>
        <div class="h-screen w-[32rem]">
          <img src="assets/images/collegium-window-and-door-person.jpg" alt="" class="w-full h-full object-cover">
        </div>
        <div class="h-screen w-[32rem]">
          <img src="assets/images/maza-gilde-2.jpg" alt="" class="w-full h-full object-cover">
        </div>
        <div class="h-screen w-[32rem]">
          <img src="assets/images/maza-gilde-2.jpg" alt="" class="w-full h-full object-cover">
        </div>
        <div class="h-screen w-[32rem]">
          <img src="assets/images/maza-gilde-2.jpg" alt="" class="w-full h-full object-cover">
        </div>
        <div class="h-screen w-[32rem]">
          <img src="assets/images/maza-gilde-2.jpg" alt="" class="w-full h-full object-cover">
        </div>
        <div class="h-screen w-[32rem]">
          <img src="assets/images/maza-gilde-2.jpg" alt="" class="w-full h-full object-cover">
        </div>


      </HeroSlider>

    </div>


    <div class="hidden  second-layer absolute w-full h-full hero-overlay"
         style=""
    ></div>



    <div
        :class="firstBackground ? '-translate-y-[110vh] ' : ' '"
        class="absolute w-full h-full transition-all duration-1000 ease-in-out  ">

      <div class="absolute flex justify-center items-center w-full h-full">
        <img src="assets/images/clothes.webp" alt="" class="w-full h-full object-cover">
      </div>

      <div
          :class="fadeBlack ? 'fade-black' : ' bg-black'"
          class="absolute w-full h-full "

      ></div>
    </div>
    <div class="third-layer absolute w-full h-full ">
        <div class="heading-element flex justify-center items-start w-full  h-[80%] ">
          <div class="ax-w-screen-2xl mx-4 pt-20  ">
            <h1 class="page-titl leading-none text-[3rem] sm:text-[5rem] md:text-[10vw] lg:text-[8vw]  text-white font-bold -translate-y-20   uppercase  text-left    cd">
              Rīgas Vēsturiskās mūzikas un dejas festivāls <br> 2025</h1>
            <p class="page-titl text-end mr-8 uppercase text-white font-semibold text-[2rem] md:text-[4vw] lg:text-[3vw] cd">6 - 11 Septembris</p>
          </div>
        </div>
      <div class="button-space h-[20%] ">

      </div>
    </div>




    <div class="button-layer absolute flex justify-center items-end w-full h-full  ">
      <div class="flex justify-center items-center h-[20%] py-2 px-2 ">

      </div>

    </div>

  </div>
</template>

<style scoped>


.heading-element {


}
@keyframes circular-reveal {

}


.hero-overlay{
  background: #000000;

  background: radial-gradient(circle, rgba(0, 0, 0, 0) 0%, rgba(0, 0, 0, 0) 58%, rgba(28, 28, 27, 1) 91%);}


.page-title{
  color: #FFFFFF;


  text-shadow: 1px 1px 1px #3d3c3c,
  -1px -1px 1px #525151,

  -3px -3px 1px #162512,
  3px 3px 2px #1f3118,
  4px 4px 3px #360000,
  -4px -4px 3px #3f0205,
  6px 6px 7px #f8992d,
  -6px -6px 7px #f8992d,
  8px 8px 9px #f8992d,
  -8px -8px 9px #f8992d,
  10px 10px 20px #e3d7c9,
  -10px -10px 20px #dcd0c6
;
}

.open-left-element{
  animation: open-left 1s ease-in;
  opacity: 0;
  display: none;

}
@keyframes open-left {
  0%{
    display: flex;
    opacity: 1;
    transform: translateX(0);
  }
  99%{
    display: flex;
    opacity: 0;
    transform: translateX(-100vw);
  }
  100%{
    display: none;
    transform: translateX(-100vw);
  }

}

.open-right-element{
  animation: open-right 2s ease-in;
  opacity: 0;
  display: none;

}
@keyframes open-right {
  0%{
    display: flex;
    opacity: 1;
    transform: translateX(0);
  }
  99%{
    display: flex;
    opacity: 0;
    transform: translateX(100vw);
  }
  100%{
    display: none;
    transform: translateX(100vw);
  }

}

.fade-black{

  background-color: rgba(9,9,9,1);
  animation: fade-black-animation 2s linear;
}

@keyframes fade-black-animation {
  0%{
    background-color: rgba(9,9,9,1);

  }
  70%{
    background-color: rgba(9,9,9,0);

  }
  80%{
    background-color: rgba(9,9,9,1);
  }
  100%{
    background-color: rgba(9,9,9,1);
  }

}

</style>