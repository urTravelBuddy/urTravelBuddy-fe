<script setup>
const emit = defineEmits(['signIn'])
const props = defineProps({
  dialogClass: String
})

const signIn = () => {
  emit('signIn')
}
</script>

<template>
  <q-card bordered :class="props.dialogClass">
    <div class="column flex-center justify-around full-height">
      <h4 class="no-padding no-margin text-primary text-bold">
        LOGO
      </h4>
      <div class="home__dialog--text text-center text-secondary q-px-lg">
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
  </q-card>
</template>

<style scoped>
</style>
