<template>
  <span class="section-subtitle">My recent works</span>
  <h2 class="section-title">Portfolio</h2>

  <div class="portfolio__nav">
    <span class="portfolio__item active-portfolio" data-filter="all">All</span>
    <span class="portfolio__item" data-filter=".web">Web</span>
    <span class="portfolio__item" data-filter=".ux">UI/UX</span>
    <span class="portfolio__item" data-filter=".des">Design</span>
  </div>

  <div class="portfolio__container bd-grid">
    <template v-for="block in content.body" v-bind:key="block._uid">
      <component :is="block.component" :block="block"></component>
    </template>
  </div>
</template>



<script>
import HelloWorld from "./components/HelloWorld.vue";
import Web from "./components/Web";
import Ux from "./components/Ux";
import Des from "./components/Des";

export default {
  name: "App",
  components: {
    HelloWorld,
    Web,
    Ux,
    Des,
  },
  data() {
    return {
      content: {
        body: [
          {
            id: 1,
            component: "web",
            slika_link:
              "https://ogden_images.s3.amazonaws.com/www.observertoday.com/images/2020/08/29003327/SUNSET-579x840.jpg",
            subtitle: "kratki opis prvog rada",
            title: "Something new",
            link: "https://www.kunkalabs.com/mixitup/docs/get-started/",
          },
          {
            id: 2,
            component: "web",
            slika_link:
              "https://ogden_images.s3.amazonaws.com/www.observertoday.com/images/2020/08/29003327/SUNSET-579x840.jpg",
            subtitle: "kratki opis drugog rada",
            title: "Drugi rad",
            link: "https://www.kunkalabs.com/mixitup/docs/get-started/",
          },
          {
            id: 3,
            component: "ux",
            slika_link:
              "https://ogden_images.s3.amazonaws.com/www.observertoday.com/images/2020/08/29003327/SUNSET-579x840.jpg",
            subtitle: "kratki opis treceg rada",
            title: "treci rad",
            link: "https://www.kunkalabs.com/mixitup/docs/get-started/",
          },
          {
            id: 4,
            component: "ux",
            slika_link:
              "https://ogden_images.s3.amazonaws.com/www.observertoday.com/images/2020/08/29003327/SUNSET-579x840.jpg",
            subtitle: "kratki opis cetvrtog rada",
            title: "cetvrti rad ",
            link: "https://www.kunkalabs.com/mixitup/docs/get-started/",
          },
          {
            id: 5,
            component: "des",
            slika_link:
              "https://ogden_images.s3.amazonaws.com/www.observertoday.com/images/2020/08/29003327/SUNSET-579x840.jpg",
            subtitle: "kratki opis petog rada",
            title: "peti rad",
            link: "https://www.kunkalabs.com/mixitup/docs/get-started/",
          },
          {
            id: 6,
            component: "des",
            slika_link:
              "https://ogden_images.s3.amazonaws.com/www.observertoday.com/images/2020/08/29003327/SUNSET-579x840.jpg",
            subtitle: "kratki opis sestog rada",
            title: "sesti rad",
            link: "https://www.kunkalabs.com/mixitup/docs/get-started/",
          },
        ],
      },
    };
  },
};
</script>




<style>
</style>
