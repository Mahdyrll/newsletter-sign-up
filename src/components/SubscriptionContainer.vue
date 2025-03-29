<script setup>
import { Form, Field, ErrorMessage } from 'vee-validate';
import * as yup from 'yup';
import { ref } from 'vue';
import { defineEmits } from 'vue';

// Define validation schema
const schema = yup.object({
    email: yup.string().email('Valid format required').required('Email is required'),
});

const emit = defineEmits(["form-success"]);

// success message
// const isSuccess = ref(false);

// handle form submission
const submitButtonHandler = () => {
    emit("form-success");
};
</script> 

<template>
    <div>
        <Form @submit="submitButtonHandler" :validation-schema="schema" class="grid gap-y-2">
            <div class="flex justify-between">
                <label for="email" class="font-robotoBold text-[13px] text-gray-700">Email address</label>
                <ErrorMessage name="email" class="text-[13px] font-robotoBold text-red-400" />
            </div>
            <Field
                id="email"
                name="email"
                type="email"
                placeholder="email@company.com"
                class="w-full h-14 border-gray-300 border-solid border-[1px] rounded-lg px-6 placeholder:font-robotoRegular focus:border-[#242742] outline-none transition-all duration-300 ease-in-out"
            />
            <button type="submit" class="bg-[#242742] font-robotoBold text-white rounded-lg px-7 py-4 mt-5 text-[15px] tracking-wide sm:transition sm:duration-300 sm:hover:bg-gradient-to-l from-[#EC6735] to-[#E94C78]">Subscribe to monthly newsletter</button>
        </Form>
    </div>
</template>