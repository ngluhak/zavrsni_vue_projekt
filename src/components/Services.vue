<template>
  <section class="services section bd-container" id="services">
    <span class="section-subtitle">What I offer</span>
    <h2 class="section-title">Services</h2>

    <div class="services__container bd-grid">
      <div class="services__data">
        <i class="bx bx-palette services__icon"></i>
        <h3 class="services__title">UI/UX Design</h3>
        <p class="services__description">iuafuasdifdfbdfbgdsfu</p>
        <a href="#" class="button">Know more</a>
      </div>

      <div class="services__data">
        <i class="bx bx-palette services__icon"></i>
        <h3 class="services__title">Graphic Design</h3>
        <p class="services__description">iuafuasdifdfbdfbgdsfu</p>
        <a href="#" class="button">Know more</a>
      </div>

      <div class="services__data">
        <i class="bx bx-palette services__icon"></i>
        <h3 class="services__title">Web Design</h3>
        <p class="services__description">iuafuasdifdfbdfbgdsfu</p>
        <a href="#" class="button">Know more</a>
      </div>
    </div>
  </section>
  <!--
            <button > open popup</button>
            <Popup v-if="popupTriggers.buttonTrigger">
                <h2>My popup</h2>
            </Popup>
-->
</template>

<script>
import { ref } from "vue";

//import Popup from './Popup.vue';

export default {
  name: "Services",

  /* 
  setup(){
      const popupTriggers = ref({
          buttonTrigger: false,
      })

      return{
          Popup,
          popupTriggers
      }
  }
  */
};
</script>
