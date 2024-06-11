<template>
  <main class="background">
    <div class="flex items-center justify-center h-screen">
      <Card />
    </div>
  </main>
</template>
<script setup>
import Card from "./components/Card.vue"
if (
  localStorage.getItem("color-theme") === "dark" ||
  (!("color-theme" in localStorage) &&
    window.matchMedia("(prefers-color-scheme: dark)").matches)
) {
  document.documentElement.classList.add("dark")
} else {
  document.documentElement.classList.remove("dark")
}
</script>

<style scoped>
.background {
  background-image: url(https://i.ibb.co.com/wgz08Q5/night.jpg);
  background-size: cover;
}
</style>
