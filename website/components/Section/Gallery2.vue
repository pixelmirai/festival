<script setup lang="js">
import {useInView} from "~/composables/useInView.js";

const inView = ref(false)
const gallery = ref(null);


onMounted(()=>{
  if (gallery.value){
    useInView(gallery.value,()=>{
      inView.value = true;
    })
  } else {
    setTimeout(()=>{
      inView.value = true;
    },500)
  }

})
</script>

<template>
<div class="relative w-[100vw] h-[48rem]  bg-white overflow-clip    ">

  <div class="first-layer absolute w-full h-full flex justify-center items-center">

    <div class="side-images absolute flex justify-between  items-center max-w-screen-2xl w-full h-full  ">
      <div class=" h-[85%] md:h-[55%] xl:h-full">
        <img src="assets/images/maza-gilde-ink.png" alt="" class="h-full  object-contain ">
      </div>
      <div class="h-[85%] md:h-[55%] xl:h-full ">
        <img src="assets/images/magdalenas-baznica.png" alt="" class="h-full  object-contain ">
      </div>
    </div>

    <div class="central-rectangle absolute w-[360px] h-[32rem] border-4 border-black  ">
      <div class="absolute w-full  h-full opacity-80">
        <img src="assets/images/collegium-door-ink-writing.png" alt="" class="w-full h-full object-cover  ">
      </div>
      <div class="absolute w-1/2 h-full">
        <img src="assets/images/violin-splash.png" alt="" class="w-full h-full object-cover  ">
      </div>
    </div>

  </div>


  <div ref="gallery" class="second-layer gallery absolute flex justify-center items-center w-full h-full object-cover  ">
    <div class="perspective   relative  opacity-75  ">
      <div  class="  container relative overflow-y-clip  w-[360px] grid grid-cols-2 gap-2   ">
        <div v-for="i in 8 "
             :class="{'translate-y-[44rem]' : !inView}"
             style="transition-duration: 5s"
             class=" w-full flex justify-center items-center aspect-square  ease-in-out ">
          <img src="assets/images/orchestra-church.webp" alt="" class="image">
        </div>
      </div>
    </div>
  </div>

</div>
</template>

<style scoped>
.perspective{
  perspective: 1200px;
}


  .container{
    transform: rotateZ(50deg) rotateX(40deg)  rotateY(-50deg) ;
  }






</style>