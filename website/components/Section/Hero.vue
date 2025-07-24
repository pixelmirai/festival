<script setup lang="js">
import {useUtils} from "~/composables/useUtils.js";
import ButtonProgramm from "~/components/ButtonProgramm.vue";


const utils = useUtils()


const heroSlider = ref(null);
const sliderInterval = ref(null)
const sliderIntervalCounter = ref(0)

const scrolled = ref(false)

defineExpose({

})

onMounted(()=>{
  window.addEventListener('scroll',()=>{
    scrolled.value = true;
  })

})

const open = ref(false)
const fadeBlack = ref(false)
const firstBackground = ref(false)
const sliderFadeOut = ref(false)
function slideOpen(){

}


</script>

<template>
  <div class="relative w-full h-full overflow-hidden min-h-[475px] xl:min-h-[600px]  ">


    <div class="first-layer absolute flex w-full h-full overflow-hidden slider-fade-out">
      <div class="absolute w-full h-full overflow-x-hidden">
        <div class="absolute h-full flex flex-nowrap min-w-max slider-movement ">
          <div  class="slider-image-size">
            <img src="assets/images/maza-gilde.jpg" alt="" class="w-full h-full object-cover">
          </div>
          <div  class="slider-image-size">
            <img src="assets/images/orchestra-church.webp" alt="" class="w-full h-full object-cover">
          </div>
          <div  class="slider-image-size">
            <img src="assets/images/maris-kupcs-2.webp" alt="" class="w-full h-full object-cover">
          </div>

          <div  class="slider-image-size">
            <img src="assets/images/elina-simkus.jpg" alt="" class="w-full h-full object-cover">
          </div>
          <div  class="slider-image-size">
            <img src="assets/images/erik-bosgraf.jpg" alt="" class="w-full h-full object-cover">
          </div>
          <div  class="slider-image-size">
            <img src="assets/images/monta-martinsone.jpg" alt="" class="w-full h-full object-cover">
          </div>
          <div  class="slider-image-size">
            <img src="assets/images/anete-viluma.jpg" alt="" class="w-full h-full object-cover">
          </div>
          <div  class="slider-image-size">
            <img src="assets/images/mauro.jpg" alt="" class="w-full h-full object-cover">
          </div>
          <div  class="w-[64rem] h-full ">
            <img src="assets/images/collegium-2.jpg" alt="" class="w-full h-full object-cover">
          </div>




        </div>
      </div>
    </div>



    <div class="first-background first-background-slide-up  absolute block  w-full h-full transition-all duration-1000 ease-in-out  ">
      <div class="absolute flex justify-center items-center w-full h-full">
        <img src="assets/images/maza-gilde-orchestra.webp" alt="" class="w-full h-full object-cover">
      </div>
      <div class="fade-black absolute w-full h-full "></div>
    </div>


    <div class="third-layer absolute w-full h-full ">
      <div class="w-full h-full flex flex-col ">

        <div class="header-space  w-full h-[4rem]"></div>

        <div class="heading-element max-w-screen-4xl mx-auto px-4  flex flex-col  flex-grow justify-between  w-full   ">

          <h1
              class="hidde  heading page-titl leading-none  text-white font-bold   transition-transform duration-1000   uppercase  text-left    cd">
            Rīgas Vēsturiskās mūzikas un dejas festivāls <br> 2025
          </h1>
          <p class="hidde date date-slide-in text-end  uppercase text-white font-semibold">6 - 11 Septembris</p>

        </div>

        <div class="button-space flex justify-center items-center w-full h-[8rem] ">
<!--          <ButtonProgramm class="" />-->
        </div>
      </div>


    </div>


  </div>
</template>

<style scoped>





/* --- For heading --- */
@media (aspect-ratio: 1/1) {
  .heading {
    font-size: 10vw;
  }
}

@media (max-aspect-ratio: 9999/10000) {
  /* ---vert --- */
  .heading {
    font-size: 12vw;
  }
}

@media (min-aspect-ratio: 10000/9999) {
  /* ---hor --- */
  .heading {
    font-size: 12vh;
  }
}

/* --- For date --- */
@media (aspect-ratio: 1/1) {
  .date {
    font-size: 4vw;
  }
}

@media (max-aspect-ratio: 9999/10000) {
  /* ---vert --- */
  .date {
    font-size: 6vw;
  }
}

@media (min-aspect-ratio: 10000/9999) {
  /* ---hor--- */
  .date {
    font-size: 6vh;
  }
}



.fade-black{
  background-color: rgba(9,9,9,1);
  animation: fade-black-animation 1.5s linear 0s forwards;
}
.first-background-slide-up {
  opacity: 1;
  visibility: visible;
  animation: fbsu 500ms linear 1.5s forwards; /* 3s delay before it begins */
}

.slider-movement{
  animation: sm 20s  forwards 1s;
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
  animation: sfo 8s linear forwards;
}

.slider-image-size{
  width: 28rem;
  height: 100vh;
}

.date-slide-in{
  opacity: 1;
  transform: translateX(0rem);
  animation: date-slide-in-animation 1s ease-out forwards;
}
@keyframes date-slide-in-animation {
  0%{
    opacity: 0;
    transform: translateX(-10rem);
  }20%
     {
       opacity: 0;
       transform: translateX(-10rem);
     }
     100%{
       opacity: 1;
       transform: translateX(0rem);
     }
}


@keyframes sfo {
  0% {
    opacity: 1;
    visibility: visible;
  }
  20%{
    opacity: 1;
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
  40%{
       background-color: rgba(9,9,9,1);
     }
  50%{
    background-color: rgba(9,9,9,0);
  }
  60%{
    background-color: rgba(9,9,9,0.5);
  }
  90%{
    background-color: rgba(9,9,9,1);

  }
  100%{
    background-color: rgba(9,9,9,1);
  }

}

</style>