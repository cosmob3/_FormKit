<template>
  <div class="flex justify-center gap-6">
    <img
      src="https://images.pexels.com/photos/1549528/pexels-photo-1549528.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
      alt="Trash"
      class="w-1/2"
    />
    <h2 class="flex text-3xl max-w-md items-center">{{ text }}</h2>
  </div>
</template>

<script setup>
const text = "You can't spell TRASH without ASH";
</script>
