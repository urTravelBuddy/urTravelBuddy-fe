<script setup>
const emit = defineEmits(['signIn'])

const signIn = () => {
  emit('signIn')
}
</script>

<template>
  <div class="column flex-center justify-around full-height">
    <div class="no-padding no-margin text-primary text-bold text-h4">
      LOGO
    </div>
    <div class="home__dialog--text text-center text-bold text-secondary q-px-lg">
      {{ $t('welcomeMessage') }}
    </div>
    <div class="full-width text-right q-pr-lg">
      <q-btn
        size="lg"
        class="bg-primary text-white q-px-lg"
        push
        rounded
        :label="$t('start')"
        @click="signIn()"
      >
      </q-btn>
    </div>
  </div>
</template>

<style scoped>
</style>
