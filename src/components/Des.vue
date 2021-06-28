<template>
  <div class="portfolio__content mix des">
    <hr />

    <a href="#"
      ><img :src="block.slika_link" alt="slikica" class="portfolio__img"
    /></a>
    <div class="portfolio__data">
      <span class="portfolio__subtitle">{{ block.subtitle }}</span>
      <a href="#"
        ><h2 class="portfolio__title">{{ block.title }}</h2></a
      >
      <a :href="block.link" class="button button-link">View details</a>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    block: Object,
  },
  name: "des",
};
</script>