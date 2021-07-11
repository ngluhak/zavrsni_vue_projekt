<template>
  <header
    class="l-header "
    id="header"
    style="padding-top: 20px !important; padding-bottom: 20px !important;
    "
  >
    <nav class="nav bd-container">
      <a href="#" class="nav__logo">Nina Gluhak</a>

      <div class="nav__menu" id="nav-menu">
        <ul class="nav__list">
          <li class="nav__item">
            <a href="#home" class="nav__link active-link">Home</a>
          </li>
          <li class="nav__item">
            <a href="#about" class="nav__link">About</a>
          </li>
          <li class="nav__item">
            <a href="#services" class="nav__link">Services</a>
          </li>
          <li class="nav__item">
            <a href="#portfolio" class="nav__link">Portfolio</a>
          </li>
          <li class="nav__item">
            <a href="#contact" class="nav__link">Contact</a>
          </li>
        </ul>
      </div>

      <div class="nav__toggle" id="nav-toggle">
        <i class="bx bx-menu"></i>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>
