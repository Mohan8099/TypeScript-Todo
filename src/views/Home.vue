<template>
  <div class="home">
    <HomeView msg="Welcome to To-do App"/>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import HomeView from '@/components/HomeView.vue'; 

export default defineComponent({
  name: 'Home',
  components: {
    HomeView,
  },
});
</script>
