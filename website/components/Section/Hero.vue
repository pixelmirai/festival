<script setup lang="js">
import {useUtils} from "~/composables/useUtils.js";


const utils = useUtils()


const heroSlider = ref(null);
const sliderInterval = ref(null)
const sliderIntervalCounter = ref(0)
defineExpose({

})

onMounted(()=>{

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


</script>

<template>
  <div class="relative w-full h-full min-h-[500px] lg:min-h-[800px] overflow-hidden">

    <div class="first-layer absolute flex w-full h-full overflow-hidden slider-fade-out">

      <div class="absolute w-full h-full overflow-x-hidden">

        <div class="absolute h-full flex flex-nowrap min-w-max slider-movement ">
          <div v-for="i in 10" class="h-[100vh] w-[32rem]">
            <img src="assets/images/maza-gilde-2.jpg" alt="" class="w-full h-full object-cover">
          </div>
        </div>

      </div>

    </div>



    <div
          class="first-background first-background-slide-up  absolute block  w-full h-full transition-all duration-1000 ease-in-out  ">

      <div class="absolute flex justify-center items-center w-full h-full">
        <img src="assets/images/clothes.webp" alt="" class="w-full h-full object-cover">
      </div>

      <div class="fade-black absolute w-full h-full "></div>
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






  </div>
</template>

<style scoped>




.fade-black{
  background-color: rgba(9,9,9,1);
  animation: fade-black-animation 1s linear 0s forwards;
}
.first-background-slide-up {
  opacity: 1;
  visibility: visible;
  animation: fbsu 500ms linear 1s forwards; /* 3s delay before it begins */
}

.slider-movement{
  animation: sm 20s  forwards;
}
@keyframes sm {
  from{
    transform: translateX(0);
  }
  to{
    transform: translateX(-100%);
  }

}


.slider-fade-out {
  opacity: 0.8;
  visibility: visible;
  animation: sfo 6s linear forwards;
}



@keyframes sfo {
  0% {
    opacity: 0.8;
    visibility: visible;
  }
  99% {
    opacity: 0;
    visibility: visible;
  }
  100% {
    opacity: 0;
    visibility: hidden;
  }
}


@keyframes fbsu {
  0% {
    transform: translateY(0);
    opacity: 1;
    visibility: visible;
  }
  99% {
    transform: translateY(-120vh);
    opacity: 1;
    visibility: visible;
  }
  100% {
    transform: translateY(-120vh);
    opacity: 0;
    visibility: hidden;
  }
}





@keyframes fade-black-animation {
  0%{
    background-color: rgba(9,9,9,1);

  }
  70%{
    background-color: rgba(9,9,9,0);

  }
  100%{
    background-color: rgba(9,9,9,1);
  }

}

</style>