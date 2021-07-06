<template>
  <section class="contact section bd-container" id="contact">
    <span class="section-subtitle">Contact</span>
    <h2 class="section-title">Contact me</h2>

    <div class="contact__container bd-grid">
      <div class="contact__content bd-grid">
        <div class="contact__box">
          <i class="bx bxs-home contact__icon"></i>
          <h3 class="contact__title">Location</h3>
          <span class="contact__description">Zagreb - Hrvatska</span>
        </div>
      </div>

      <div class="contact__content bd-grid">
        <div class="contact__box">
          <i class="bx bxs-phone contact__icon"></i>
          <h3 class="contact__title">Phone</h3>
          <span class="contact__description">092-1105-282</span>
        </div>
      </div>

      <div class="contact__content bd-grid">
        <div class="contact__box">
          <i class="bx bxs-envelope contact__icon"></i>
          <h3 class="contact__title">Email</h3>
          <span class="contact__description">ninaa.gluhak@gmail.com</span>
        </div>
      </div>

      <div class="contact__content bd-grid">
        <div class="contact__box">
          <i class="bx bxs-chat contact__icon"></i>
          <h3 class="contact__title">Chat</h3>

          <div>
            <a href="#" class="contact__social"
              ><i class="bx bxl-whatsapp-square"></i
            ></a>
            <a
              href="https://www.facebook.com/profile.php?id=100014190482633"
              class="contact__social"
              ><i class="bx bxl-messenger"></i
            ></a>
            <a
              href="https://www.linkedin.com/in/nina-gluhak-6212b81ba/"
              class="contact__social"
              ><i class="bx bxl-linkedin"></i
            ></a>
          </div>
        </div>
      </div>

      <form action="" class="contact__form" @submit.prevent="handleSubmit">
        <div class="contacts__inputs">
          <input
            type="text"
            placeholder="Name"
            class="contact__input"
            required
            v-model="name"
          />
          <div v-if="nameError" class="error">{{ nameError }}</div>

          <input
            type="email"
            placeholder="Email"
            class="contact__input"
            required
            v-model="email"
          />
        </div>
        <div class="contacts__inputs">
          <input
            type="text"
            placeholder="Project"
            class="contact__input"
            v-model="project"
          />
          <input
            type="text"
            placeholder="Skills needed"
            class="contact__input"
            v-model="tempSkill"
            @keyup.alt="addSkill"
          />
          <div v-for="skill in skills" :key="skill" class="pill">
            <span @click="deleteSkill(skill)">{{ skill }}</span>
          </div>
        </div>

        <textarea
          name=""
          id=""
          cols="0"
          rows="7"
          placeholder="Message"
          class="contact__input"
          v-model="mess"
        ></textarea>

        <div class="terms">
          <input type="checkbox" v-model="terms" />
          <label>Subscribe for more news and updates</label>
        </div>

        <input
          type="submit"
          value="Send Message"
          class="button contact__button"
        />
      </form>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      email: "",
      project: "",
      tempSkill: "",
      skills: [],
      nameError: "",
      terms: false,
      mess: "",
    };
  },
  methods: {
    addSkill(e) {
      if (e.key === "," && this.tempSkill) {
        if (!this.skills.includes(this.tempSkill)) {
          this.skills.push(this.tempSkill);
        }
        this.tempSkill = "";
      }
    },
    deleteSkill(skill) {
      this.skills = this.skills.filter((item) => {
        return skill !== item;
      });
    },
    handleSubmit() {
      //name validation
      this.nameError =
        this.name.length > 2 ? "" : "Name must have at least 2 characters";
      if (!this.nameError) {
        console.log("name:", this.name);
        console.log("email:", this.email);
        console.log("project:", this.project);
        console.log("skills:", this.skills);
        console.log("mess:", this.mess);
        console.log("terms:", this.terms);
      }
    },
  },
};
</script>

<style scoped>
.pill {
  display: inline-block;
  margin: 5px 10px 10px 0;
  padding: 6px 12px;
  background: #f1dfdf;
  border-radius: 20px;
  font-size: 12px;
  letter-spacing: 1px;
  font-weight: bold;
  color: #a44e07;
  cursor: pointer;
}

.error {
  margin-bottom: 10px;
  margin-left: 5px;
  color: #6f2804;

  font-weight: bold;
}

.terms {
  margin-bottom: 10px;
}

.terms label {
  margin-left: 5px;
  color: #a44e07;
}
</style>
