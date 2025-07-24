<script setup lang="ts">
import {useInView} from "~/composables/useInView";

const inView = ref(false)
const section = ref(null)
const text1 = "Rīgas Vēsturiskās mūzikas un dejas festivāls 2025 ir starptautisks kultūras notikums, kas notiks no 6. septembra līdz 11. oktobrim dažādās Rīgas koncertvietās."
const text2 = " Festivāls piedāvā bagātīgu programmu ar senās mūzikas koncertiem, koncertlekcijām un garīgās mūzikas notikumiem, pulcējot augsta līmeņa māksliniekus no Latvijas un ārzemēm. Tajā uzstāsies tādi atzīti kolektīvi kā Collegium Musicum Riga, Neymann Ensemble, Regence Sonore un Coloquio 6, kā arī ievērojami solisti, piemēram, Ēriks Bosgrāfs, Elīna Šimkus un Mauro Pinciaroli."

onMounted(()=>{
  if(section.value){
    useInView(section.value,()=>{
      inView.value = true;
    })
  }

})

</script>

<template>
<div ref="section" class=" flex flex-col-reverse md:flex-row py-16   "
style="background-color: #ffffff"
>

  <div class="flex justify-center items-center w-full  md:w-1/2 min-w-[360px] ">
      <div class="w-[300px] border border-black  " style="aspect-ratio: 10/16">

      </div>
  </div>
  <div class="flex justify-center items-center w-full  md:w-1/2 min-w-[360px] ">

    <div class="p-8  ">
      <div class="overflow-clip pb-2 pr-2  ">
        <div
            :class="{'description-text-shadow':inView}"
            class="flex flex-col pb-16 pr-16   gap-12  ">
          <p class="text-5xl font-semibold text-center">{{text1}}</p>
          <p class="text-xl ">{{text2}}</p>
        </div>
      </div>
    </div>
  </div>

</div>
</template>

<style scoped>
.description-text-shadow{
  opacity: 1;
  box-shadow: black -5rem 2px 0,
  black 2px -2rem 0;
  animation: description-text-shadow-fade 2s ease-out forwards;
}
@keyframes description-text-shadow-fade {
  from{
    opacity: 0;
    box-shadow: black -30rem 2px 0,
    black 2px -30rem 0;
  }
  to {
    opacity: 1;
    box-shadow: black -5rem 2px 0,
    black 2px -2rem 0;
  }
}
</style>