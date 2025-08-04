<script setup lang="ts">

</script>

<template>
  <div class="w-screen bg-black">
    <div class="w-screen ">
      <div class="flex  w-[96rem] mx-auto py-[8rem] ">
        <div class="h-[40rem] aspect-square  ">
          <div class="flex justify-start w-full h-1/2">
            <ContactMK/>
          </div>
          <div class="flex justify-end  w-full h-1/2">
            <ContactAD/>
          </div>


        </div>
        <div class="flex flex-col  justify-center items-center w-[16rem] h-[20rem] ">
          <ContactSocialIcons/>
          <div class="text-white uppercase text-xl font-extrabold py-4 ">
            <span>seko mums</span>
          </div>
        </div>
        <div class="flex flex-col justify-center items-center h-[40rem] aspect-square    ">
          <div class="flex flex-col justify-center items-center w-1/2 aspect-square  ">
            <div class="w-[16rem]  ">
              <img src="assets/images/logo.webp" alt="" class="w-full h-full">
            </div>
            <div class="flex justify-center items-center text-2xl text-white whitespace-nowrap   ">
              <span class="font-extralight -translate-y-[2px] ">SIA </span> <span class="italic font-serif  ml-1 "> Rīgas Senās mūzikas centrs</span>
            </div>

            <div class="flex flex-col justify-center items-center text-white h-1/3  ">
              <div class="  text-5xl hover:opacity-75 transition-opacity duration-300 ">
                <a  href="https://maps.app.goo.gl/Ee2kDv5G3qYuEzRBA" >
                  <svg xmlns="http://www.w3.org/2000/svg" width="1.5rem" height="" fill="currentColor" class="bi bi-map" viewBox="0 0 16 16">
                    <path fill-rule="evenodd" d="M15.817.113A.5.5 0 0 1 16 .5v14a.5.5 0 0 1-.402.49l-5 1a.5.5 0 0 1-.196 0L5.5 15.01l-4.902.98A.5.5 0 0 1 0 15.5v-14a.5.5 0 0 1 .402-.49l5-1a.5.5 0 0 1 .196 0L10.5.99l4.902-.98a.5.5 0 0 1 .415.103M10 1.91l-4-.8v12.98l4 .8zm1 12.98 4-.8V1.11l-4 .8zm-6-.8V1.11l-4 .8v12.98z"/>
                  </svg>
                </a>
              </div>
              <div class="text-xl hover:underline  ">
                <a href="https://maps.app.goo.gl/Ee2kDv5G3qYuEzRBA" >
                <span>Vaļņu iela 9-3, Rīga, LV-1050</span>
                </a>
              </div>
            </div>

          </div>
          <div class="h-1/2 aspect-square">
            <iframe class="w-full h-full" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2598.0651446728034!2d24.107608077161537!3d56.95025799912953!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x46eecfd124d75647%3A0x184f72b13af16db9!2zVmHEvMWGdSBpZWxhIDksIENlbnRyYSByYWpvbnMsIFLEq2dhLCBMVi0xMDUwLCBMYXR2aWE!5e1!3m2!1sen!2sat!4v1754053100948!5m2!1sen!2sat" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
          </div>

        </div>
      </div>
    </div>

  </div>


</template>

<style scoped>

</style>