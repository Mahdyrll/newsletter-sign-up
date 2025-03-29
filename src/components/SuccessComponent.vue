<script setup>
defineEmits(["reset"]);
</script>

<template>
    <div class="pt-36 pb-7 bg-white sm:text-center sm:flex sm:flex-col sm:w-fit sm:mx-auto sm:rounded-[2rem] sm:shadow-lg sm:py-14 sm:mt-10">
        <div class="pl-7 pr-6 grid gap-y-6 sm:px-16">
            <img src="../assets/images/icon-success.svg" alt="success">
            <h2 class="font-robotoBold text-4xl text-[#242742] mt-5 sm:w-64 sm:text-left sm:text-[45px] ">Thanks for subscribing!</h2>
            <p class="font-robotoRegular text-base sm:w-96 sm:text-left">A confirmation email has been sent to <b class="font-robotoBold text-base">ash@loremcompany.com</b>. Please open it and click the button inside to confirm your subscription</p>
        </div>
        <div class="text-center mt-40 sm:mt-10">
            <button @click="$emit('reset')" class="bg-[#242742] font-robotoBold text-white tracking-wide px-24 py-4 rounded-lg sm:px-32 sm:hover:bg-gradient-to-l from-[#EC6735] to-[#E94C78] sm:transition sm:duration-300">Dismiss message</button>
        </div>
    </div>
</template>