<script setup lang="ts">
defineProps<{
  msg: string
}>()
</script>

<template>
  <div class="greetings">
    <h1 class="green">{{ msg }}</h1>
    <h3 class="subtitle">
      You've successfully created a
      <a
        href="https://dev.viz-it.int.bayer.com/webserver/portletce-docs/"
        target="_blank"
        rel="noopener"
        >Viz-it Portlet</a
      >
      project with <br />
      <a href="https://vite.dev/" target="_blank" rel="noopener">Vite</a> +
      <a href="https://vuejs.org/" target="_blank" rel="noopener">Vue 3</a> +
      <a href="https://quasar.dev/" target="_blank" rel="noopener">Quasar</a>.
      <p class="mt-4">
        Visit the
        <a href="https://dev.viz-it.int.bayer.com/webserver/gallery/" target="_blank" rel="noopener"
          >Portlet Gallery</a
        >
        for more portlet examples.
      </p>
    </h3>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 300;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
  color: rgb(134, 205, 27);
}

h3 {
  font-size: 1.2rem;
}

.subtitle {
  font-weight: 400;
  line-height: 1.4;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
