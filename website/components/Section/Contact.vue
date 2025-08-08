<script setup lang="js">
const w = ref(0)

onMounted(()=>{
  w.value = window.innerWidth;
  window.addEventListener('resize',()=>{
    w.value =  window.innerWidth
  })
})
</script>

<template>
  <div class="bg-black">
    <div class="bg-white">
      inner w : {{w}}
    </div>
    <ContactSM class="contact-sm" />
    <ContactMD class="contact-md" />
    <ContactLG class="contact-lg" />
  </div>
</template>

<style scoped>
/* Hide/show based on Tailwind's default breakpoints */

/* Default: small version visible */
.contact-sm {
  display: block;
}
.contact-md,
.contact-lg {
  display: none;
}

/* md: ≥768px → show medium, hide small */
@media (min-width: 768px) {
  .contact-sm {
    display: none;
  }
  .contact-md {
    display: block;
  }
}

/* 2xl: ≥1536px → show large, hide medium */
@media (min-width: 1536px) {
  .contact-md {
    display: none;
  }
  .contact-lg {
    display: block;
  }
}
</style>
