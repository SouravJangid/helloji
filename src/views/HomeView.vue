<script setup lang="ts">
import TopView from '../components/atop.vue'
import FormView from '../components/bform.vue'
import DownView from '../components/cdown.vue'
</script>

<template>
  <div class="main">
    <TopView />
    <FormView />
    <DownView />
  </div>
</template>
<style>
.main{
  display:grid;
  grid-template-rows: auto auto auto;
  gap: 5%;
}
</style>