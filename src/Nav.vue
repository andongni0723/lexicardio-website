<script setup>
import {onMounted, onUnmounted, ref} from "vue";
import {useRouter} from "vue-router";

const isScroll = ref(false);
const router = useRouter();
const version = __APP_VERSION__

const handleScroll = () =>
{
  isScroll.value = window.scrollY > 50;
}

onMounted(() =>
{
  window.addEventListener('scroll', handleScroll);
})

onUnmounted(() =>
{
  window.removeEventListener('scroll', handleScroll);
})
</script>

<template>
<div class="fixed m-0 top-0 w-screen bg-transparent transition-colors duration-500 flex flex-col justify-between z-[900]"
     :class="{'!bg-background': isScroll}">
  <div class="py-5 px-[8%] flex justify-between items-center">
    <!-- Logo -->
    <div class="flex items-center gap-20">
      <img class="h-[64px] object-contain select-none"
           src="/lexicardio.webp" alt="">
      <h1 class="w-auto wrap-normal text-light-white text-2xl font-poppins">Lexicardio</h1>
      <p class="text-primary-dark text-sm font-poppins">v{{version}}</p>
    </div>

    <a class="bg-primary hover:bg-primary-dark transition p-10 px-15 text-sm rounded-full text-light-white font-poppins"
       href="https://github.com/andongni0723/Lexicardio/releases/latest">
      Download
    </a>
  </div>
  <hr v-show="isScroll" class="text-primary-dark m-0">
</div>
</template>

<style scoped>

</style>
