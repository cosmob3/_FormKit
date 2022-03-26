<template>
  <div class="flex flex-wrap justify-center gap-6">
    <div>
      <a
        href="https://cosmob3.github.io/404-page/"
        class="text-4xl bg-yellow-200 rounded-xl p-3"
        >Click at your own risk</a
      >
    </div>
    <img
      src="https://images.pexels.com/photos/1549528/pexels-photo-1549528.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
      alt="Trash"
      class="w-auto rounded-xl"
    />
    <h2
      class="flex text-3xl max-w-md items-center justify-self-auto text-center"
    >
      {{ text }}
    </h2>
  </div>
</template>

<script setup>
const text = "You can't spell TRASH without ASH";
</script>
