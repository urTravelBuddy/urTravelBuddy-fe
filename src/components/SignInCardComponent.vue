<script setup>
import { ref } from 'vue'

const isPwd = ref(true)
const password = ref('')
</script>

<template>
  <div class="row">
    <div class="col-12 text-center text-secondary q-mt-lg">
      <div class="no-padding no-margin text-bold text-h5">{{ $t('signIn') }}</div>
    </div>
  </div>
  <q-separator color="grey" class="q-mt-sm" inset />
  <div class="row q-mt-lg">
    <div class="col-10 offset-1">
      <q-input outlined dense label="Email"></q-input>
    </div>
  </div>
  <div class="row q-mt-lg">
    <div class="col-10 offset-1">
      <q-input
        outlined
        dense
        v-model="password"
        label="Password" :type="isPwd ? 'password' : 'text'">
        <template v-slot:append>
          <q-icon
            :name="isPwd ? 'visibility_off' : 'visibility'"
            class="cursor-pointer"
            @click="isPwd = !isPwd"
          />
        </template>
      </q-input>
    </div>
  </div>
</template>

<style scoped>
</style>
