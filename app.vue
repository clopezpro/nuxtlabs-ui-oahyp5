<script setup lang="ts">
const items = [
  {
    label: 'Activity',
    key: 'activity',
  },
  {
    label: 'Rate Activity',
    key: 'rateActivity',
  },
];
const tabActive = ref(0);
function nextRate(next: number) {
  tabActive.value = next;
}
</script>

<template>
  TAB ASYNC IS: <span>{{ tabActive }}</span>
  <UTabs v-model="tabActive" :items="items" />

  <div class="flex justify-center">
    <UButton
      label="GOT TO TAG 1"
      color="red"
      variant="solid"
      @click="nextRate(1)"
    />
  </div>
</template>
