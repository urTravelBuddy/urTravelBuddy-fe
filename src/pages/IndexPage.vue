<script setup>
import { ref } from 'vue'
import WelcomeCardComponent from 'components/WelcomeCardComponent'
import SignInCardComponent from 'components/SignInCardComponent'

let component = WelcomeCardComponent
const isDialogOpen = ref(true)
const isSeamless = ref(true)
const dialogClass = ref('home__dialog')

const signIn = () => {
  dialogClass.value = 'home__dialog--maximized'
  isSeamless.value = false
  component = SignInCardComponent
}

</script>
<template>
  <q-page>
  </q-page>
  <q-dialog
    position="bottom"
    persistent
    :seamless="isSeamless"
    full-width
    transition-duration="1000"
    v-model="isDialogOpen"
  >
    <q-card bordered :class="dialogClass">
      <component :is=component @signIn="signIn()" class="no-padding"></component>
    </q-card>
  </q-dialog>
</template>

<style scoped>
</style>
