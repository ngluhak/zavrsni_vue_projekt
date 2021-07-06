<template>
  <section class="home" id="home">
                <div class="home__container bd-container bd-grid">
                    <div class="home__data">
                        <span class="home__greeting">Hello, my name is</span>
                        <h1 class="home__name">Nina Gluhak</h1>
                        <span class="home__profession">Web developer</span>
                        <a download="" href="assets/pdf/Gluhak_CV_2021.pdf" class="button button-light ">Download CV</a>
                    </div>

                    <div class="home__social">
                        <a href="https://www.facebook.com/profile.php?id=100014190482633" class="home__social-icon"><i class='bx bxl-facebook-square' ></i></a>
                        <a href="#" class="home__social-icon"><i class='bx bxl-instagram' ></i></a>
                        <a href="https://www.linkedin.com/in/nina-gluhak-6212b81ba/" class="home__social-icon"><i class='bx bxl-linkedin' ></i></a>
                    </div>

                    <div class="home__img">
                        <img src="../assets/img/maca1.jpg" alt="" class="">
                    </div>
                </div>
            </section>
</template>

<script>
export default {
  name: "Home",
};
</script>