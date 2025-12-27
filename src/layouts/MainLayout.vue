<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-toolbar-title>
          <img
            src="/logo.svg"
            alt="Dicerollapp Logo"
            style="width: 24px; height: 24px; margin-right: 8px; vertical-align: middle"
          />
          Dicerollapp
        </q-toolbar-title>

        <div>v1.0.0</div>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
// No menu needed
</script>
