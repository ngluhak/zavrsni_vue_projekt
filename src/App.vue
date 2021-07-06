<template>
  <a href="#" class="scrolltop" id="scroll-top">
    <i class="bx bxs-chevron-up scrolltop__icon"></i>
  </a>

  <Header />

  <main class="l-main">
    <Home />
    <About />
    <Qualification />
    <Services />

    <section class="portfolio section bd-container" id="portfolio">
      <span class="section-subtitle">My recent works</span>
      <h2 class="section-title">Portfolio</h2>

      <div class="portfolio__nav">
        <span class="portfolio__item active-portfolio" data-filter="all"
          >All</span
        >
        <span class="portfolio__item" data-filter=".web">Web</span>
        <span class="portfolio__item" data-filter=".ux">UI/UX</span>
        <span class="portfolio__item" data-filter=".des">Design</span>
      </div>

      <div class="portfolio__container bd-grid">
        <template v-for="block in content.body" v-bind:key="block._uid">
          <component :is="block.component" :block="block"></component>
        </template>
      </div>
    </section>

    <Contact />
  </main>

  <Footer />
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Web from "./components/Web";
import Ux from "./components/Ux";
import Des from "./components/Des";
import Header from "./components/Header";
import Home from "./components/Home";
import About from "./components/About";
import Qualification from "./components/Qualification";
import Services from "./components/Services";
import Contact from "./components/Contact";
import Footer from "./components/Footer";

export default {
  name: "App",
  components: {
    HelloWorld,
    Web,
    Ux,
    Des,
    Header,
    Home,
    About,
    Qualification,
    Services,
    Contact,
    Footer,
  },

  data() {
    return {
      content: {
        body: this.fetchTasks(),

        /* [
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
        ],*/
      },
    };
  },

  methods: {
    async fetchTasks() {
      const res = await fetch("http://localhost:5000/body");
      const data = await res.json();
      return data;
    },
  },

  /*
  async created() {
    this.body = await this.fetchTasks();
  },
  */

  mounted() {
    let skripta = document.createElement("script");
    skripta.setAttribute("href", "./assets/js/mixitup.min.js");
    document.head.appendChild(skripta);
  },
};
</script>

<style></style>
