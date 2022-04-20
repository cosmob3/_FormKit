<script setup>
import { ref } from "vue";
const submitted = ref(false);
const formData = ref({});
const submitHandler = async () => {
  // Let's pretend this is an ajax request:
  await new Promise((r) => setTimeout(r, 1000));
  submitted.value = true;
};
</script>

<template>
  <div class="flex justify-center">
    <FormKit
      type="form"
      v-model="formData"
      :form-class="submitted ? 'hide' : 'show'"
      submit-label="Submit"
      @submit="submitHandler"
      submit-label-class="bg-grey-700 text-white"
    >
      <h1 class="text-4xl font-semibold">Get in touch!</h1>
      <p>
        If you are interested or have any questions, email me or fill out the
        form below and I’ll get back to you within 48 hours..
      </p>
      <hr class="pb-10" />

      <FormKit
        type="text"
        name="name"
        label="Full Name"
        placeholder="Jane Doe"
        help="What do people call you?"
        validation="required"
        outer-class="mb-5"
        label-class="block mb-1 font-bold text-sm"
        inner-class="max-w-md border border-gray-400 rounded-lg mb-1 overflow-hidden focus-within:border-blue-500"
        input-class="w-full h-10 px-3 border-none text-base text-gray-700 placeholder-gray-400"
        help-class="text-xs text-gray-500"
      />
      <FormKit
        type="text"
        name="email"
        label="Your email"
        placeholder="jane@example.com"
        help="What email should we use?"
        validation="required|email"
        :classes="{
          outer: 'mb-5',
          label: 'block mb-1 font-bold text-sm',
          inner:
            'max-w-md border border-gray-400 rounded-lg mb-1 overflow-hidden focus-within:border-blue-500',
          input:
            'w-full h-10 px-3 border-none text-base text-gray-700 placeholder-gray-400',
          help: 'text-xs text-gray-500',
        }"
      />
      <FormKit
        type="textarea"
        name="text"
        label="Message"
        validation="required"
        placeholder="What can I do for you"
        help="A short message letting me know what you are looking for"
        :classes="{
          outer: 'mb-5',
          inner:
            'max-w-md h-24 border border-gray-400 rounded-lg mb-1 overflow-hidden focus-within:border-blue-500',
          input:
            'w-full h-24 px-3 border-none text-base text-gray-700 placeholder-gray-400',
          label: 'block mb-1 font-bold text-sm',
          help: 'text-xs text-gray-500',
        }"
      />
    </FormKit>
  </div>
  <div class="flex justify-center gap-y-14" v-if="submitted">
    <h2>Submission successful!</h2>
  </div>
  <pre class="text-center" wrap>{{ formData }}</pre>
</template>
