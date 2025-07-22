<script setup lang="js">
import {useUtils} from "~/composables/useUtils.js";


const utils = useUtils()

defineExpose({
  animate
})

onMounted(()=>{
  //animate()
})

const open = ref(false)
const firstBackground = ref(false)
function slideOpen(){

}

function animate(){
  setTimeout(()=>{
    firstBackground.value = true
  },1000)
  setTimeout(()=>{
   open.value = true;
  },2000)



}

</script>

<template>
  <div class="relative w-full h-full ">

    <div class="first-layer absolute flex w-full h-full ">

      <div
          :class="{ 'open-left-element': open }"
          class="left-side relative flex w-1/2 h-full overflow-hidden ">

        <div class="absolute flex flex-row-reverse    right-0  w-[50vw] h-full">
          <div class="main-left-image w-full md:w-1/2 h-full  bg-teal-300 ">
            <img src="assets/images/maza-gilde-2.jpg"  alt=""
                 class="w-full h-full object-cover"
            >
          </div>
          <div class="hidden md:block  md:w-1/2 h-full  bg-teal-300 ">
            <img src="assets/images/maza-gilde-orchestra.webp"  alt=""
                 class="w-full h-full object-cover object-[75%_center]"
            >
          </div>

        </div>

      </div>

      <div
          :class="{ 'open-right-element': open }"
          class="right-side relative flex w-1/2 h-full overflow-hidden ">

        <div class=" absolute flex    left-0  w-[50vw] h-full">
          <div class=" main-right-image w-full md:w-1/2 h-full  bg-teal-300 ">
            <img src="assets/images/collegium-window.jpg"  alt=""
                 class="w-full h-full object-cover"
            >
          </div>
          <div class="hidden md:block  md:w-1/2 h-full  bg-teal-300 ">
            <img src="assets/images/maris-kupcs-baroque-1.webp"  alt=""
                 class="w-full h-full object-cover "
            >
          </div>
        </div>


      </div>

    </div>


    <div class="hidden  second-layer absolute w-full h-full hero-overlay"
         style=""
    ></div>



    <div
        :class="firstBackground ? '-translate-y-[110vh]' : ''"
        class="absolute w-full h-full transition-all duration-1000 ease-in-out ">

      <div class="absolute flex justify-center items-center w-full h-full">
        <img src="assets/images/clothes.webp" alt="" class="w-full h-full object-cover">
      </div>

      <div class="absolute w-full h-full "
      style="background-color: rgba(9,9,9,0)"
      ></div>



    </div>
    <div class="third-layer absolute w-full h-full ">
        <div class="heading-element flex justify-center items-start w-full h-full  ">
          <div class="ax-w-screen-2xl mx-4 pt-20  ">
            <h1 class="page-titl leading-none text-white font-bold -translate-y-20 transition-all duration-1000 ease-linear  uppercase  text-left    text-[8vw] cd">
              Rīgas Vēsturiskās mūzikas un dejas festivāls <br> 2025</h1>
            <p class="page-titl text-end mr-8 uppercase text-white font-semibold text-[3vw] cd">6 - 11 Septembris</p>
          </div>
        </div>
    </div>
    <div class="button-layer absolute flex justify-center items-end w-full h-full py-8 px-4 ">
        <div class="bg-white p-8"><button>programma</button></div>
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
  animation: open-left 2s ease-in;
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

</style>