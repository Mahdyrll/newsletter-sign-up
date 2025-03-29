<script setup>
import ListComponent from './ListComponent.vue';
import SubscriptionContainer from './SubscriptionContainer.vue';

defineEmits(["form-success"]);
</script>

<template>
    <div class="pb-4 sm:flex sm:flex-row-reverse sm:w-fit sm:mx-auto sm:items-center sm:bg-white sm:rounded-[2rem] sm:p-5 sm:shadow-lg">
      <div>
        <img class="sm:hidden w-full" src="../assets/images/illustration-sign-up-mobile.svg" alt="illustration">
        <img class="hidden sm:block" src="../assets/images/illustration-sign-up-desktop.svg" alt="desktop">
      </div>
      <div class="px-7 py-9 sm:mr-4 sm:px-10">
        <div class="">
          <h2 class="font-robotoBold text-[40px] text-[#242742] sm:text-[47px]">Stay updated!</h2>
          <p class="text-base font-robotoRegular text-gray-700 mt-3 sm:w-96">Join 60,000+ product managers receiving monthly updates on:</p>
        </div>
        <div>
          <ListComponent />
        </div>
        <div>
          <SubscriptionContainer @form-success="$emit('form-success')" class="mt-8" />
        </div>
      </div>
    </div>
</template>