<script setup lang="js">
import {useInView} from "~/composables/useInView.js";

const inView = ref(false)
const gallery = ref(null);

const IMG_URL = "https://rvmdfcontent.wordpress.com/wp-content/uploads/2025/08/";
const gilde = IMG_URL + "page-maza-gilde-ink.webp"
const magdalena = IMG_URL + "page-magdalenas-baznica.webp"
const door = IMG_URL + "page-collegium-door-ink-green-2-2.webp"
const splash = IMG_URL + "page-violin-splash-2.webp"

const images = {
  bosgraf: IMG_URL + 'gallery-bosgraf.webp',
  bosgrafCollegium: IMG_URL + 'gallery-bosgraf-collegium.webp',
  coloquio6: IMG_URL + 'gallery-coloquio6.webp',
  kupcsMartinsone: IMG_URL + 'gallery-kupcs-martinsone.webp',
  neymannEnsemble3: IMG_URL + 'gallery-neymann-ensemble-3.webp',
  regenceSonore: IMG_URL + 'gallery-regence-sonore.webp',
  revalers: IMG_URL + 'gallery-revalers.webp',
};

onMounted(()=>{
  if (gallery.value){
    useInView(gallery.value,()=>{
      inView.value = true;
    },0.3)
  }
})
</script>



<template>
<div class="relative w-[100vw] h-[48rem]  bg-white overflow-clip    ">

  <div class="first-layer absolute w-full h-full flex justify-center items-center">

    <div class="side-images absolute flex justify-between  items-center max-w-screen-2xl w-full h-full  ">
      <div class=" h-[85%] md:h-[55%] xl:h-full">
        <img :src="gilde" loading="lazy" alt="" class="fade-in h-full  object-contain ">
      </div>
      <div class="h-[85%] md:h-[55%] xl:h-full ">
        <img :src="magdalena" loading="lazy" alt="" class="fade-in h-full  object-contain ">
      </div>
    </div>

    <div class="central-rectangle absolute w-[360px] h-[32rem] border-4 border-black  ">
      <div class="absolute w-full  h-full opacity-80">
        <img :src="door" loading="lazy" alt="" class="fade-in  w-full h-full object-cover  ">
      </div>
      <div class="absolute w-1/2 h-full">
        <img :src="splash" loading="lazy" alt="" class="fade-in w-full h-full object-cover  ">
      </div>
    </div>

  </div>


  <div ref="gallery" class="second-layer gallery absolute flex justify-center items-center w-full h-full object-cover  ">
    <div class="perspective   relative  opacity-75  ">
      <div   class="  container relative overflow-y-clip  w-[360px] grid grid-cols-2 gap-2   ">


        <div
             :class="{'translate-y-[44rem]' : !inView}"
             style="transition-duration: 5s"
             class=" w-full flex justify-center items-center aspect-square  ease-in-out ">
          <img :src="images.bosgrafCollegium" loading="lazy" alt="" class="image">
        </div>

        <div
            :class="{'translate-y-[44rem]' : !inView}"
            style="transition-duration: 5s"
            class=" w-full flex justify-center items-center aspect-square  ease-in-out ">
          <img :src="images.coloquio6" alt="" loading="lazy" class="image">
        </div>

        <div
            :class="{'translate-y-[44rem]' : !inView}"
            style="transition-duration: 5s"
            class=" w-full flex justify-center items-center aspect-square  ease-in-out ">
          <img :src="images.kupcsMartinsone" alt="" loading="lazy" class="image">
        </div>
        <div
            :class="{'translate-y-[44rem]' : !inView}"
            style="transition-duration: 5s"
            class=" w-full flex justify-center items-center aspect-square  ease-in-out ">
          <img :src="images.revalers" alt="" loading="lazy" class="image">
        </div>




        <div
            :class="{'translate-y-[44rem]' : !inView}"
            style="transition-duration: 5s"
            class=" w-full flex justify-center items-center aspect-square  ease-in-out ">
          <img :src="images.regenceSonore" alt="" loading="lazy" class="image">
        </div>


        <div
            :class="{'translate-y-[44rem]' : !inView}"
            style="transition-duration: 5s"
            class=" w-full flex justify-center items-center aspect-square  ease-in-out ">
          <img :src="images.neymannEnsemble3" alt="" loading="lazy" class="image">
        </div>

        <div
            :class="{'translate-y-[44rem]' : !inView}"
            style="transition-duration: 5s"
            class=" col-span-2 w-full flex justify-center items-center   ease-in-out ">
          <img :src="images.bosgraf" alt="" loading="lazy" class="image">
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

.fade-in{
  animation: fade-in 1s ease-in-out forwards;
}

@keyframes fade-in {
  from{
    opacity: 0;
  }
  to{
    opacity: 1;
  }
  
}




</style>