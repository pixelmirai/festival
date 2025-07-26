<script setup lang="js">
import {useWpPosts} from "~/stores/useWpPosts.js";
import {useHTMLContent} from "~/composables/useHTMLContent.js";

const wpPosts = useWpPosts();
const html = useHTMLContent();
const images = ref([]);

async function getImages(){
  try {
    const response = await wpPosts.getPost({slug: "gallery-1"});
    if (response){
      images.value = Object.values(response.attachments).map(a => a.URL);
      console.log(images.value);
    }
  }catch (e) {
    console.log(e)
  }
}

onMounted(async ()=>{
 await getImages()
})

</script>

<template>
<div class=" background  w-screen grid grid-cols-2 sm:grid-cols-3 xl:grid-cols-4   ">
  <div v-for="i in 12"  class="flex justify-center items-center w-full    border-transparent " style="aspect-ratio: 1.6;">
      <div class="w-full h-full m-2 sm:m-2 lg:m-2      bg-blue-950">
        <img src="https://rvmdfcontent.wordpress.com/wp-content/uploads/2025/07/neymann-ensemble.jpg" alt=""
        class="w-full h-full object-cover"
        >
      </div>
  </div>
</div>
</template>

<style scoped>

.background{
  background-color: rgba(6, 38, 133, 0.5);

}
</style>