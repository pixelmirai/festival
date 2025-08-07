<script setup lang="js">
import {useInView} from "~/composables/useInView.js";

const inView = ref(false)
const gallery = ref(null);


onMounted(()=>{
  if (gallery.value){
    useInView(gallery.value,()=>{
      inView.value = true;
    },0.2)
  }

})
</script>

<template>
  <div>


  <div class="relative w-[100vw] h-[36rem]    bg-white overflow-x-clip    ">
    <div class="first-layer absolute w-full h-full flex justify-center items-center">

      <div class="central-rectangle absolute w-[320px]  border-2  border-black  " style="aspect-ratio: 0.65">
        <div class="absolute w-full  h-full opacity-80">
          <img src="assets/images/collegium-door-ink-writing.png" alt="" class="w-full h-full object-cover  ">
        </div>
        <div class="absolute w-1/2 h-full">
          <img src="assets/images/violin-splash.png" alt="" class="w-full h-full object-cover  ">
        </div>
      </div>

    </div>


    <div
        ref="gallery"
        class="second-layer gallery absolute flex justify-center items-center w-full h-full object-cover  ">
      <div class="perspective   relative  opacity-75  ">
        <div class=" container relative overflow-y-clip  w-[240px] grid grid-cols-2 gap-2   ">
          <div
              :class="{'translate-y-[44rem]' : !inView}"
              style="transition-duration: 5s"
              class=" w-full flex justify-center items-center aspect-square  ease-in-out ">
            <img src="assets/images/gallery/bosgraf-collegium-stage.jpg" alt="" class="image">
          </div>

          <div
              :class="{'translate-y-[44rem]' : !inView}"
              style="transition-duration: 5s"
              class=" w-full flex justify-center items-center aspect-square  ease-in-out ">
            <img src="assets/images/gallery/coloquio6-2.png" alt="" class="image">
          </div>

          <div
              :class="{'translate-y-[44rem]' : !inView}"
              style="transition-duration: 5s"
              class=" w-full flex justify-center items-center aspect-square  ease-in-out ">
            <img src="assets/images/gallery/kupcs-martinsone.jpg" alt="" class="image">
          </div>
          <div
              :class="{'translate-y-[44rem]' : !inView}"
              style="transition-duration: 5s"
              class=" w-full flex justify-center items-center aspect-square  ease-in-out ">
            <img src="assets/images/gallery/revalers.png" alt="" class="image">
          </div>




          <div
              :class="{'translate-y-[44rem]' : !inView}"
              style="transition-duration: 5s"
              class=" w-full flex justify-center items-center aspect-square  ease-in-out ">
            <img src="assets/images/gallery/regence-sonore-3.png" alt="" class="image">
          </div>


          <div
              :class="{'translate-y-[44rem]' : !inView}"
              style="transition-duration: 5s"
              class=" w-full flex justify-center items-center aspect-square  ease-in-out ">
            <img src="assets/images/gallery/neymann-ensemble-3.jpg" alt="" class="image">
          </div>

          <div
              :class="{'translate-y-[44rem]' : !inView}"
              style="transition-duration: 5s"
              class=" col-span-2 w-full flex justify-center items-center   ease-in-out ">
            <img src="assets/images/bosgraf-long.png" alt="" class="image">
          </div>

        </div>
      </div>
    </div>

  </div>
  <div>
    <div class="side-images flex justify-between  items-center w-full h-full bg-white ">
      <div class=" ">
        <img src="assets/images/maza-gilde-ink.png" alt="" class="h-full  object-contain ">
      </div>
      <div class="">
        <img src="assets/images/magdalenas-baznica.png" alt="" class="h-full  object-contain ">
      </div>
    </div>
  </div>
  </div>
</template>

<style scoped>
.perspective{
  perspective: 800px;
}


.container{
  transform: rotateZ(30deg) rotateX(30deg)  rotateY(-30deg) ;
}





</style>