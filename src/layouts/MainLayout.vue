<script setup>
</script>

<template>
  <q-layout view="hHh lpR fFf">

    <q-header v-if="false" reveal elevated class="bg-primary text-white">
      <q-toolbar>
        <q-toolbar-title class="text-center">
          Header
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-page-container class="bg-layout">
      <router-view />
    </q-page-container>

    <q-footer v-if="false" elevated class="bg-primary text-white">
      <q-toolbar>
        <q-toolbar-title class="text-center">
          Footer
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>

  </q-layout>
</template>
