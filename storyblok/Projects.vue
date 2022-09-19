<script setup >
defineProps ({
  blok: Object,
});
</script>

<template>
  <div class = "container project-page">
    <div class = "project-title">
      <h1> {{ blok.name || "New Projects" }} </h1>
      <NuxtLink :to="{ name : 'index' }"> Go Back </NuxtLink>
    </div>
    <div class="project-description">
      <img :src="blok.image?.filename || 'https://picsum.photos/300/175'" :alt="blok.image?.alt"/>
      <p> {{ blok.description || "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce quis fermentum ante, vel vestibulum lectus. Etiam pharetra quis sem non bibendum. Nulla tincidunt molestie enim quis suscipit. Etiam hendrerit libero vel elit maximus pellentesque. Sed imperdiet nunc eu justo interdum commodo." }} </p>
    </div>
  </div>
</template>
