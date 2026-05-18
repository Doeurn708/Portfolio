<script setup lang="ts">
import Layouts from './layouts/Layouts.vue'
import { RouterView } from 'vue-router'
</script>

<template>
  <div>
    <Layouts>
      <RouterView />
    </Layouts>
  </div>
</template>