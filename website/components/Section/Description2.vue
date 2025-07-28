<script setup lang="ts">
const text = " Festivāls piedāvā bagātīgu programmu ar senās mūzikas koncertiem, koncertlekcijām un garīgās mūzikas notikumiem, pulcējot augsta līmeņa māksliniekus no Latvijas un ārzemēm. Tajā uzstāsies tādi atzīti kolektīvi kā Collegium Musicum Riga, Neymann Ensemble, Regence Sonore un Coloquio 6, kā arī ievērojami solisti, piemēram, Ēriks Bosgrāfs, Elīna Šimkus un Mauro Pinciaroli."

</script>

<template>
<div class="w-full bg-white">
  <div class="max-w-screen-2xl mx-auto px-2  flex flex-wrap min-h-[32rem] border-t-2 border-gray-300 ">
      <div class="w-1/2 min-w-[360px] flex justify-center items-center">
          <article>
            <p class="text-xl  font-serif">
              {{text}}
            </p>

          </article>
      </div>
      <div class="w-1/2 min-w-[360px] flex justify-center items-center">
        <div class="image-thing relative h-[24rem] " style="aspect-ratio: 10/16">
          <div class="absolute w-full h-full rounded-t-full overflow-clip">
            <img src="assets/images/collegium-window-and-door-person.jpg" alt="" class="w-full h-full object-cover">
          </div>
          <div class="absolute w-full h-full rounded-t-full overflow-clip hover:opacity-0 transition-opacity duration-1000">
            <img src="assets/images/collegium-door-person-gray.webp" alt="" class="w-full h-full object-cover">
          </div>
        </div>
      </div>

  </div>

</div>
</template>

<style scoped>

</style>