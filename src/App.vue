<script setup>
import Header from "./components/Header.vue";
import CardMain from "./components/CardMain.vue";
import SocialIcons from "./components/SocialIcons.vue";
import Experience from "./components/Experience.vue";
import Work from "./components/Work.vue";
import { ref, onMounted } from 'vue';
import ProgressSpinner from "primevue/progressspinner";

const loading = ref(true);

onMounted(async () => {
  setTimeout(() => {
    loading.value = false;
  }, 1500);
});
</script>

<template>
  <div v-if="loading" class="flex items-center justify-center h-screen">
    <ProgressSpinner style="width: 50px; height: 50px" strokeWidth="8" fill="transparent" animationDuration=".5s"
      aria-label="Loading" />
  </div>
  <div v-else>
    <Header />
    <CardMain />
    <SocialIcons />
    <Experience />
    <Work />
  </div>
</template>
