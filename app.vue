<script setup>
const items = [
  {
    label: 'Datos Actividad',
    key: 'activity',
  },
  {
    label: 'Calificar',
    key: 'rateActivity',
  },
];
const tabActive = ref(0);
function nextRate() {
  tabActive.value = 1;
}
</script>

<template>
  <UTabs v-model="tabActive" :items="items">
    <template #item="{ item }">
      <UCard>
        <template #header>
          <pre>{{ tabActive }}</pre>
        </template>

        <div v-if="item.key === 'activity'" class="space-y-3">
          <div class="border border-gray-800 p-2 rounded-md">
            <UButton
              label="next"
              color="gray"
              variant="solid"
              @click="nextRate"
            />
          </div>
        </div>
        <div v-else-if="item.key === 'rateActivity'" class="space-y-3">
          <h1>RATE</h1>
        </div>
      </UCard>
    </template>
  </UTabs>
</template>
