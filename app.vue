<script setup>
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
function nextRate() {
  tabActive.value = 1;
}
</script>

<template>
  TAB ASYNC IS: <span>{{ tabActive }}</span>
  <UTabs v-model="tabActive" :items="items" />
</template>
