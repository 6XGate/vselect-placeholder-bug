<template>
  <VContainer class="fill-height">
    <VResponsive class="d-flex align-center text-center fill-height">
      <VSelect v-model="item" label="Item" :items="items" placeholder="required"/>
    </VResponsive>
  </VContainer>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import { readonly } from 'vue';

const items = readonly([
  { title: 'Item one', value: 'i1' },
  { title: 'Item one', value: 'i1' },
  { title: 'Item one', value: 'i1' }
])

type Item = typeof items[number]

const item = ref<Item>()
</script>
