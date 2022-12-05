<script setup>
import { ref } from 'vue'
import WelcomeCardComponent from 'components/WelcomeCardComponent'
import SignInCardComponent from 'components/SignInCardComponent'

const component = WelcomeCardComponent
const isDialogOpen = ref(true)
const isSeamless = ref(true)
const dialogClass = ref('home__dialog')

const signIn = () => {
  dialogClass.value = 'home__dialog--maximized'
  isSeamless.value = false
  component.value = SignInCardComponent
}

</script>
<template>
  <q-page>
  </q-page>
  <q-dialog
    position="bottom"
    :seamless="isSeamless"
    full-width
    transition-duration="1000"
    v-model="isDialogOpen"
  >
    <component :is=component :dialog-class="dialogClass" @signIn="signIn()"></component>
  </q-dialog>
</template>

<style scoped>
</style>
