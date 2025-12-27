<template>
  <q-page class="old-style flex flex-center column q-gutter-md">
    <h1>Dicerollapp</h1>
    <h2>Created by Mahdi Ruiz</h2>

    <q-select
      v-model="dice"
      :options="diceOptions"
      label="Select a dice"
      emit-value
      map-options
      style="width: 200px"
    />

    <q-btn @click="rollDice" :disable="!dice" label="Roll Dice" color="primary" />

    <p v-if="result" class="text-h6">You rolled: {{ result }}</p>
  </q-page>
</template>

<script setup>
import { ref } from 'vue'

const dice = ref('')
const result = ref(null)

const diceOptions = [
  { label: 'D4', value: '4' },
  { label: 'D6', value: '6' },
  { label: 'D8', value: '8' },
  { label: 'D10', value: '10' },
  { label: 'D12', value: '12' },
  { label: 'D20', value: '20' },
]

const rollDice = () => {
  if (!dice.value) return
  result.value = Math.floor(Math.random() * parseInt(dice.value)) + 1
}
</script>
