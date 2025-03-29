<script setup>
const items = [
    "Product discovery and building what matters",
    "Measuring to ensure updates are a success",
    "and much more"
];
</script>

<template>
    <div class="mt-6">
        <ul class="gap-3 grid">
            <li v-for="(item, index) in items" :key="index" class="flex">
                <span><img src="../assets/images/icon-list.svg" alt="list" class="w-6"></span>
                <span class="font-robotoRegular text-base text-gray-700 ml-4">{{ item }}</span>
            </li>
        </ul>
    </div>
</template>