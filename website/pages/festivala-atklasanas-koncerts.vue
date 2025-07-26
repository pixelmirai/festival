<script setup lang="ts">
import {useRouter} from "vue-router";
const mazaGilde = "https://maps.app.goo.gl/1VRCZxZ65KwyMzXXA"
const collegiumZale = "https://maps.app.goo.gl/qxiCgmYymshP3jz67"
const magdalena = "https://maps.app.goo.gl/sbecYuJLmT3JSpFn6"
const bolderaja = "https://maps.app.goo.gl/2hNPemBN7wiASMgN6"
const router = useRouter();
</script>

<template>
<div class="max-w-screen-2xl mx-auto">

  <section class="mt-20 ">

      <h1 class="text-5xl font-serif text-center  ">Festivāla atkāšanas koncerts Baltās Nakts ietvaros</h1>
    <h3 class="text-xl font-bold  italic text-center">Četri pretendenti Leipcigā: Bahs, Tēlemanis, Graupners un Fašs - virtuozā vācu baroka mūzika</h3>

    <div>

    </div>

  </section>

<section>
  <div class="program-item   mx-4   ">
    <div class="">
      <p class="font-bold text-2xl text-gray-600 uppercase "><span>6. septembris </span> <span>18:00 </span></p>
    </div>
    <div class="flex flex-col py-4   gap-2 border-b border-gray-200">
      <h2 class="text-3xl font-serif  ">Festivāla atkāšanas koncerts Baltās Nakts ietvaros</h2>
      <h3 class="text-xl font-bold  italic">Četri pretendenti Leipcigā: Bahs, Tēlemanis, Graupners un Fašs - virtuozā vācu baroka mūzika</h3>
    </div>
    <div class="pt-4 ">
      Baroka orķestris <strong class="">Collegium Musicum Riga</strong>, <strong>Ēriks Bosgrafs</strong> (Nīderlande)
      un orķestra solisti.
    </div>
    <div>
      <div class="flex justify-center py-4   ">
        <a :href="mazaGilde" target="_blank" rel="noopener noreferrer">
          <p class="hover:underline">RKTMC <span class="italic pr-2">Mazā Ģilde</span>
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor" class="bi bi-geo-alt-fill inline -translate-y-1 " viewBox="0 0 16 16">
              <path d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10m0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6"/>
            </svg>
          </p>
        </a>
      </div>
      <div class="flex  ">
        <p class="flex justify-start  items-end   w-1/2 ">
          Ieeja ar bezmaksas ielūgumiem
        </p>
        <div class="flex justify-end items-center w-1/2">
          <button
              @click="router.push('/festivala-atklasanas-koncerts')"
              class="bg-black text-white w-[6rem] hover:bg-white hover:text-black border-2 border-black  cursor-pointer  " style="aspect-ratio: 1.6">Lasīt</button>
        </div>

      </div>
    </div>
  </div>
</section>
</div>
</template>

<style scoped>

</style>