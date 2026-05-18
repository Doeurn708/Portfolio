<script setup lang="ts">
import MenuBar from '../components/MenuBar.vue'
</script>

<template>
  <div>
    <MenuBar />
    
    <main>
      <slot />
    </main>
  </div>
</template>