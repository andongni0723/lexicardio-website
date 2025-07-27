<script setup lang="ts">
import {computed} from "vue";

const props = defineProps<{
  items: string[]
  seq?: string
  wrap?: boolean
}>()

const sep = computed(() => props.seq ?? '+')
</script>

<template>
  <div class="flex flex-col items-start gap-30" :class="{ 'flex-wrap': wrap }">
    <template v-for="(tag, i) in items" :key="`${tag}`" >
      <!-- Chip -->
      <div class="group bg-container hover:bg-primary p-10 rounded-2xl flex items-center gap-20 hover:scale-[1.1] transition">
        <p class="text-primary group-hover:text-primary-dark text-7xl select-none font-poppins">#</p>
        <p class="text-light-white text-6xl select-none font-poppins">{{ tag }}</p>
      </div>
      <!-- Sep -->
      <!--<span v-if="i < items.length - 1"-->
      <!--      class="text-light-white m-3 text-2xl select-none">{{ sep }}</span>-->
    </template>
  </div>
</template>

<style scoped>
@import "@/assets/main.css";

.dark {
  @apply text-background;
}
</style>
