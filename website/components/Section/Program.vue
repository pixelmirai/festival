<script setup lang="js">
import {useRouter} from "vue-router";
const mazaGilde = "https://maps.app.goo.gl/1VRCZxZ65KwyMzXXA"
const collegiumZale = "https://maps.app.goo.gl/qxiCgmYymshP3jz67"
const magdalena = "https://maps.app.goo.gl/sbecYuJLmT3JSpFn6"
const bolderaja = "https://maps.app.goo.gl/2hNPemBN7wiASMgN6"
const router = useRouter();

const program = [
  {

  }
]

</script>

<template>
<div class="bg-white min-h-96 ">
    <div class="max-w-screen-2xl mx-auto ">
        <div class="flex flex-col  mx-auto  max-w-screen-md ">


          <div class="program-item   mx-4    ">
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

          <div class="  w-full  my-16 border-t border-black mx-4   "></div>


          <div class="program-item   mx-4    ">
            <div class="">
              <p class="font-bold text-2xl text-gray-600 uppercase "><span>13. septembris </span> <span>18:00 </span></p>
            </div>
            <div class="flex flex-col py-4   gap-2 border-b border-gray-200">
              <h2 class="text-3xl font-serif  ">Ansamblis <span class="italic">Regence Sonore</span> (Polija)</h2>
            </div>

            <div>
              <div class="flex justify-center py-4   ">
                <a :href="collegiumZale" target="_blank" rel="noopener noreferrer">
                  <p class="hover:underline">Koncertzāle: <span class="italic pr-2">Collegium Musicm Riga</span>
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor" class="bi bi-geo-alt-fill inline -translate-y-1 " viewBox="0 0 16 16">
                      <path d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10m0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6"/>
                    </svg>
                  </p>
                </a>
              </div>
              <div class="flex  ">
                <div class="flex justify-start  items-end   w-1/2 ">
                  <a href="https://www.bilesuparadize.lv/lv/event/154875" target="_blank" rel="noopener noreferrer" >
                    <button

                        class="bg-[#5B8930] border-2  border-[#5B8930] text-white w-[6rem] hover:bg-white hover:text-[#5B8930] cursor-pointer  " style="aspect-ratio: 1.6">
                      Biļetes</button>
                  </a>

                </div>
                <div class="flex justify-end items-center w-1/2">
                  <button
                      @click="router.push('/festivala-atklasanas-koncerts')"
                      class="bg-black text-white w-[6rem] hover:bg-white hover:text-black border-2 border-black  cursor-pointer  " style="aspect-ratio: 1.6">Lasīt</button>
                </div>

              </div>
            </div>
          </div>

          <div class="  w-full  my-16 border-t border-black mx-4   "></div>


          <div class="program-item   mx-4    ">
            <div class="">
              <p class="font-bold text-2xl text-gray-600 uppercase "><span>16. septembris </span> <span>19:00 </span></p>
            </div>
            <div class="flex flex-col py-4   gap-2 border-b border-gray-200">
              <h2 class="text-3xl font-serif  ">Koncerts-lekcija <span class="italic">In Exilium</span>
                , viduslaiku mūzikas ansamblis <span class="italic">Ex Silentio</span> (Grieķija)
              </h2>
            </div>

            <div>
              <div class="flex justify-center py-4   ">
                <a :href="collegiumZale" target="_blank" rel="noopener noreferrer">
                  <p class="hover:underline">Koncertzāle: <span class="italic pr-2">Collegium Musicm Riga</span>
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor" class="bi bi-geo-alt-fill inline -translate-y-1 " viewBox="0 0 16 16">
                      <path d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10m0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6"/>
                    </svg>
                  </p>
                </a>
              </div>
              <div class="flex  ">
                <div class="flex justify-start  items-end   w-1/2 ">
                  <a href="https://www.bilesuparadize.lv/lv/event/154884" target="_blank" rel="noopener noreferrer" >
                    <button

                        class="bg-[#5B8930] border-2  border-[#5B8930] text-white w-[6rem] hover:bg-white hover:text-[#5B8930] cursor-pointer  " style="aspect-ratio: 1.6">
                      Biļetes</button>
                  </a>

                </div>
                <div class="flex justify-end items-center w-1/2">
                  <button
                      @click="router.push('/festivala-atklasanas-koncerts')"
                      class="bg-black text-white w-[6rem] hover:bg-white hover:text-black border-2 border-black  cursor-pointer  " style="aspect-ratio: 1.6">Lasīt</button>
                </div>

              </div>
            </div>
          </div>

          <div class="  w-full  my-16 border-t border-black mx-4   "></div>



          <div class="program-item   mx-4    ">
            <div class="">
              <p class="font-bold text-2xl text-gray-600 uppercase "><span>20. septembris </span> <span>20:00 </span></p>
            </div>
            <div class="flex flex-col py-4   gap-2 border-b border-gray-200">
              <h2 class="text-3xl font-serif  "> <span>Neymann Ensemble</span>  (Latvija, Austrija, Itālija)</h2>
              <h3 class="text-xl font-bold  italic">Amorose ai rai del sole (Venēcijas mūzika)</h3>
            </div>

            <div>
              <div class="flex justify-center py-4   ">
                <a :href="magdalena" target="_blank" rel="noopener noreferrer">
                  <p class="hover:underline">Rīgas Svētās Marijas Magdalēnas baznīca
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor" class="bi bi-geo-alt-fill inline -translate-y-1 " viewBox="0 0 16 16">
                      <path d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10m0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6"/>
                    </svg>
                  </p>
                </a>
              </div>
              <div class="flex  ">
                <div class="flex justify-start  items-end   w-1/2 ">
                  <a href="https://www.bilesuparadize.lv/lv/event/154881" target="_blank" rel="noopener noreferrer" >
                    <button

                        class="bg-[#5B8930] border-2  border-[#5B8930] text-white w-[6rem] hover:bg-white hover:text-[#5B8930] cursor-pointer  " style="aspect-ratio: 1.6">
                      Bezmaksas IELŪGUMS</button>
                  </a>
                </div>
                <div class="flex justify-end items-center w-1/2">
                  <button
                      @click="router.push('/festivala-atklasanas-koncerts')"
                      class="bg-black text-white w-[6rem] hover:bg-white hover:text-black border-2 border-black  cursor-pointer  " style="aspect-ratio: 1.6">Lasīt</button>
                </div>

              </div>
            </div>
          </div>

          <div class="  w-full  my-16 border-t border-black mx-4   "></div>







          <div class="program-item   mx-4    ">
            <div class="">
              <p class="font-bold text-2xl text-gray-600 uppercase "><span>22. septembris </span> <span>19:00 </span></p>
            </div>
            <div class="flex flex-col py-4   gap-2 border-b border-gray-200">
              <h2 class="text-3xl font-serif  ">Koncerts <span class="italic">Stāsti (man) par mīlestību</span>
              </h2>
            </div>
            <div class="pt-4 ">
              <strong class="">Anete Viļuma</strong> (soprāns), <strong>Mauro Pinciaroli </strong> (Lauta, Itālija)

            </div>

            <div>
              <div class="flex justify-center py-4   ">
                <a :href="collegiumZale" target="_blank" rel="noopener noreferrer">
                  <p class="hover:underline">Koncertzāle: <span class="italic pr-2">Collegium Musicm Riga</span>
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor" class="bi bi-geo-alt-fill inline -translate-y-1 " viewBox="0 0 16 16">
                      <path d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10m0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6"/>
                    </svg>
                  </p>
                </a>
              </div>
              <div class="flex  ">
                <div class="flex justify-start  items-end   w-1/2 ">
                  <a href="https://www.bilesuparadize.lv/lv/event/154883" target="_blank" rel="noopener noreferrer" >
                    <button

                        class="bg-[#5B8930] border-2  border-[#5B8930] text-white w-[6rem] hover:bg-white hover:text-[#5B8930] cursor-pointer  " style="aspect-ratio: 1.6">
                      Bezmaksas IELŪGUMS</button>
                  </a>

                </div>
                <div class="flex justify-end items-center w-1/2">
                  <button
                      @click="router.push('/festivala-atklasanas-koncerts')"
                      class="bg-black text-white w-[6rem] hover:bg-white hover:text-black border-2 border-black  cursor-pointer  " style="aspect-ratio: 1.6">Lasīt</button>
                </div>

              </div>
            </div>
          </div>

          <div class="  w-full  my-16 border-t border-black mx-4   "></div>



          <div class="program-item   mx-4    ">
            <div class="">
              <p class="font-bold text-2xl text-gray-600 uppercase "><span>25. septembris </span> <span>19:00 </span></p>
            </div>
            <div class="flex flex-col py-4   gap-2 border-b border-gray-200">
              <h2 class="text-3xl font-serif  ">Koncertlekcija <span class="italic">Mocarts un sievietes viņa dzīvē (un mākslā)</span></h2>
            </div>
            <div class="pt-4 ">
              <strong class="">Māris Kupčs</strong> (lektors, klavesīns), <strong>Monta Martinsone</strong> (soprāns)
            </div>
            <div>
              <div class="flex justify-center py-4   ">
                <a :href="collegiumZale" target="_blank" rel="noopener noreferrer">
                  <p class="hover:underline">Koncertzāle: <span class="italic pr-2">Collegium Musicm Riga</span>
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor" class="bi bi-geo-alt-fill inline -translate-y-1 " viewBox="0 0 16 16">
                      <path d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10m0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6"/>
                    </svg>
                  </p>
                </a>
              </div>
              <div class="flex  ">
                <div class="flex justify-start  items-end   w-1/2 ">
                  <a href="https://www.bilesuparadize.lv/lv/event/154882" target="_blank" rel="noopener noreferrer" >
                    <button

                        class="bg-[#5B8930] border-2  border-[#5B8930] text-white w-[6rem] hover:bg-white hover:text-[#5B8930] cursor-pointer  " style="aspect-ratio: 1.6">
                      Bezmaksas IELŪGUMS</button>
                  </a>

                </div>
                <div class="flex justify-end items-center w-1/2">
                  <button
                      @click="router.push('/festivala-atklasanas-koncerts')"
                      class="bg-black text-white w-[6rem] hover:bg-white hover:text-black border-2 border-black  cursor-pointer  " style="aspect-ratio: 1.6">Lasīt</button>
                </div>

              </div>
            </div>
          </div>

          <div class="  w-full  my-16 border-t border-black mx-4   "></div>




          <div class="program-item   mx-4    ">
            <div class="">
              <p class="font-bold text-2xl text-gray-600 uppercase "><span>26. septembris </span> <span>16:00 </span></p>
            </div>
            <div class="flex flex-col py-4   gap-2 border-b border-gray-200">
              <h2 class="text-3xl font-serif  ">Garīgās mūzikas koncerts <span class="italic">Mūzika saulrieta krāsās</span></h2>
            </div>
            <div class="pt-4 ">
              <strong class="">Monta Martinsone</strong> (soprāns), <strong>Jolanta Barinska</strong> (ērgeles)
            </div>
            <div>
              <div class="flex justify-center py-4   ">
                <a :href="bolderaja" target="_blank" rel="noopener noreferrer">
                  <p class="hover:underline">Bolderājas ev.lug. baznīca
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor" class="bi bi-geo-alt-fill inline -translate-y-1 " viewBox="0 0 16 16">
                      <path d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10m0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6"/>
                    </svg>
                  </p>
                </a>
              </div>
              <div class="flex  ">
                <div class="flex justify-start  items-end   w-1/2 ">
                  <a href="https://www.bilesuparadize.lv/lv/event/154882" target="_blank" rel="noopener noreferrer" >
                    <button

                        class="bg-[#5B8930] border-2  border-[#5B8930] text-white w-[6rem] hover:bg-white hover:text-[#5B8930] cursor-pointer  " style="aspect-ratio: 1.6">
                      Bezmaksas IELŪGUMS</button>
                  </a>

                </div>
                <div class="flex justify-end items-center w-1/2">
                  <button
                      @click="router.push('/festivala-atklasanas-koncerts')"
                      class="bg-black text-white w-[6rem] hover:bg-white hover:text-black border-2 border-black  cursor-pointer  " style="aspect-ratio: 1.6">Lasīt</button>
                </div>

              </div>
            </div>
          </div>

          <div class="  w-full  my-16 border-t border-black mx-4   "></div>



          <div class="program-item   mx-4    ">
            <div class="">
              <p class="font-bold text-2xl text-gray-600 uppercase "><span>3. Oktobris </span> <span>19:00 </span></p>
            </div>
            <div class="flex flex-col py-4   gap-2 border-b border-gray-200">
              <h2 class="text-3xl font-serif  ">Itālijas Valdzinājums</h2>
            </div>
            <div class="pt-4 ">
               <strong class="">Elīna Šimkus</strong> (soprāns), <strong>Māris Kupčs</strong> (klavesīns)
            </div>
            <div>
              <div class="flex justify-center py-4   ">
                <a :href="collegiumZale" target="_blank" rel="noopener noreferrer">
                  <p class="hover:underline">Koncertzāle: <span class="italic pr-2">Collegium Musicm Riga</span>
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor" class="bi bi-geo-alt-fill inline -translate-y-1 " viewBox="0 0 16 16">
                      <path d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10m0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6"/>
                    </svg>
                  </p>
                </a>
              </div>
              <div class="flex  ">
                <div class="flex justify-start  items-end   w-1/2 ">
                  <a href="https://www.bilesuparadize.lv/lv/event/154877" target="_blank" rel="noopener noreferrer" >
                    <button

                        class="bg-[#5B8930] border-2  border-[#5B8930] text-white w-[6rem] hover:bg-white hover:text-[#5B8930] cursor-pointer  " style="aspect-ratio: 1.6">
                      Biļetes</button>
                  </a>

                </div>
                <div class="flex justify-end items-center w-1/2">
                  <button
                      @click="router.push('/festivala-atklasanas-koncerts')"
                      class="bg-black text-white w-[6rem] hover:bg-white hover:text-black border-2 border-black  cursor-pointer  " style="aspect-ratio: 1.6">Lasīt</button>
                </div>

              </div>
            </div>
          </div>




          <div class="  w-full  my-16 border-t border-black mx-4   "></div>



          <div class="program-item   mx-4    ">
            <div class="">
              <p class="font-bold text-2xl text-gray-600 uppercase "><span>5. Oktobris </span> <span>16:00 </span></p>
            </div>
            <div class="flex flex-col py-4   gap-2 border-b border-gray-200">
              <h2 class="text-3xl font-serif  ">Koncerts <span class="italic">The Revalers</span> (Igaunija)</h2>
            </div>
            <div>
              <div class="flex justify-center py-4   ">
                <a :href="collegiumZale" target="_blank" rel="noopener noreferrer">
                  <p class="hover:underline">Koncertzāle: <span class="italic pr-2">Collegium Musicm Riga</span>
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor" class="bi bi-geo-alt-fill inline -translate-y-1 " viewBox="0 0 16 16">
                      <path d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10m0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6"/>
                    </svg>
                  </p>
                </a>
              </div>
              <div class="flex  ">
                <div class="flex justify-start  items-end   w-1/2 ">
                  <a href="https://www.bilesuparadize.lv/lv/event/154878" target="_blank" rel="noopener noreferrer" >
                    <button

                        class="bg-[#5B8930] border-2  border-[#5B8930] text-white w-[6rem] hover:bg-white hover:text-[#5B8930] cursor-pointer  " style="aspect-ratio: 1.6">
                      Biļetes</button>
                  </a>

                </div>
                <div class="flex justify-end items-center w-1/2">
                  <button
                      @click="router.push('/festivala-atklasanas-koncerts')"
                      class="bg-black text-white w-[6rem] hover:bg-white hover:text-black border-2 border-black  cursor-pointer  " style="aspect-ratio: 1.6">Lasīt</button>
                </div>

              </div>
            </div>
          </div>


          <div class="  w-full  my-16 border-t border-black mx-4   "></div>

          <div class="program-item   mx-4    ">
            <div class="">
              <p class="font-bold text-2xl text-gray-600 uppercase "><span>11. Oktobris </span> <span>16:00 </span></p>
            </div>
            <div class="flex flex-col py-4   gap-2 border-b border-gray-200">
              <h2 class="text-3xl font-serif  ">Festivāla noslēguma koncerts</h2>
              <h3 class="text-xl font-bold  ">Ansamblis <span class="italic">Coloquio 6 </span>(Hāga, NL) (S-Eeemerging) </h3>
            </div>
            <div>
              <div class="flex justify-center py-4   ">
                <a :href="collegiumZale" target="_blank" rel="noopener noreferrer">
                  <p class="hover:underline">Koncertzāle: <span class="italic pr-2">Collegium Musicm Riga</span>
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor" class="bi bi-geo-alt-fill inline -translate-y-1 " viewBox="0 0 16 16">
                      <path d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10m0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6"/>
                    </svg>
                  </p>
                </a>
              </div>
              <div class="flex  ">
                <div class="flex justify-start  items-end   w-1/2 ">
                  <a href="https://www.bilesuparadize.lv/lv/event/154879" target="_blank" rel="noopener noreferrer" >
                    <button

                        class="bg-[#5B8930] border-2  border-[#5B8930] text-white w-[6rem] hover:bg-white hover:text-[#5B8930] cursor-pointer  " style="aspect-ratio: 1.6">
                      Biļetes</button>
                  </a>

                </div>
                <div class="flex justify-end items-center w-1/2">
                  <button
                      @click="router.push('/festivala-atklasanas-koncerts')"
                      class="bg-black text-white w-[6rem] hover:bg-white hover:text-black border-2 border-black  cursor-pointer  " style="aspect-ratio: 1.6">Lasīt</button>
                </div>

              </div>
            </div>
          </div>



        </div>
    </div>
</div>
</template>

<style scoped>

</style>