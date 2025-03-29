<script setup>
import { ref } from "vue";
import FormPage from './components/FormPage.vue';
import SuccessComponent from './components/SuccessComponent.vue';

const formSubmitted = ref(false);

const handleFormSuccess = () => {
  formSubmitted.value = true
};

const dismissMessage = () => {
  formSubmitted.value = false
}
</script>

<template>
  <div class="sm:bg-[#36384e] sm:h-screen sm:pt-20">
    <FormPage v-if="!formSubmitted" @form-success="handleFormSuccess" />
    <SuccessComponent @reset="dismissMessage" v-else />
  </div>
</template>

<style scoped>

</style>
