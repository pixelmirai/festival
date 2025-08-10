<script setup lang="ts">
import {useScrollHandler} from "~/composables/useScrollHandler";
import {useInView} from "~/composables/useInView";
import { useUtils } from "~/composables/useUtils";

const utils = useUtils();

const imageInView = ref(false)
const image = ref(null);

const IMG_URL = "https://rvmdfcontent.wordpress.com/wp-content/uploads/2025/08/"

const images = {
}


const hr = ref(0)

onMounted(()=>{
  if(image.value){
    useInView(image.value,()=>{
      imageInView.value = true;

    },0.8)
  }


})

</script>

<template>
<div class="w-full bg-white">
  <div class="max-w-screen-2xl mx-auto px-2 py-8   flex flex-wrap min-h-[32rem] border-t-2 border-gray-300 ">
      <div class="w-1/2 min-w-[360px] flex flex-grow  justify-center items-center my-4 ">
          <article>
            <p class=" text-xl  lg:text-2xl  font-serif">
              Festivāls piedāvā bagātīgu programmu ar senās mūzikas koncertiem, koncertlekcijām un garīgās mūzikas notikumiem, pulcējot augsta līmeņa māksliniekus no Latvijas un ārzemēm. Tajā uzstāsies tādi atzīti kolektīvi kā Collegium Musicum Riga, Neymann Ensemble, Regence Sonore un Coloquio 6, kā arī ievērojami solisti, piemēram, Ēriks Bosgrāfs, Elīna Šimkus un Mauro Pinciaroli.
            </p>

          </article>
      </div>
      <div class="w-1/2 min-w-[360px] flex flex-grow justify-center items-center  ">
        <div class="image-thing relative h-[32rem] " style="aspect-ratio: 10/16">
          <div
              :class="{'image-frame':imageInView}"
              class=" absolute w-full h-full rounded-t-full overflow-clip">
            <img src="https://rvmdfcontent.wordpress.com/wp-content/uploads/2025/08/page-collegium-door-front.webp" alt="" class="w-full h-full object-cover">
          </div>
          <div ref="image"
              :class="{'fade-in':imageInView}"
              class="absolute w-full h-full rounded-t-full overflow-clip hover:opacity-1  transition-opacity duration-1000" >
            <img src="https://rvmdfcontent.wordpress.com/wp-content/uploads/2025/08/page-collegium-door.webp" alt="" class="w-full h-full object-cover">
          </div>
        </div>
      </div>

  </div>

</div>
</template>

<style scoped>
.image-frame{

  animation: frame-shadow 5s ease-out forwards;
}
@keyframes frame-shadow {
  0%{
    box-shadow: #52524c 5px 5px 15px 15px ;
  }
  20%{
    box-shadow: #52524c 10px 15px 10px 10px ;
  }

  100%{
    box-shadow: #52524c 8px 8px 2px 0px ;
  }

}


@keyframes scroll-fade-in {
  from{
    opacity: 0;
  }to{
  opacity: 1;
     }
}

@keyframes scroll-fade-out {
  from{
    opacity: 1;
  }to{
     opacity: 0;
   }
}

.fade-in{
  animation: fade-in 5s linear forwards;
}

@keyframes fade-in {
  from{
    opacity: 1;
  }to{
     opacity: 0;
   }
}

</style>