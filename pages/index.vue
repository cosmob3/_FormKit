<template>
  <div class="flex flex-wrap justify-center gap-6">
    <div class="flex flex-col justify-center">
      <a
        href="https://cosmob3.github.io/404-page/"
        class="text-2xl md:text-4xl bg-yellow-200 rounded-xl p-3"
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
    <article class="container w-full"></article>
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  background-color: white;
}

main {
  height: auto;
}
</style>

<script setup>
const text = "You can't spell TRASH without ASH";

// const ashLens = data.find((item) => item.caption.includes("#ashlens"));

// document.querySelector(".container").innerHTML = `
// <figure>
//   <img src="${ashLens.url}" alt="Photo from instagram"
//   <figcaption>${ashLens.caption}</figcaption>
// </figure>
// `;
</script>
