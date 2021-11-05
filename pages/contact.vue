<template>
  <!-- Contact Tab -->
  <section>
    <div class="header-row">
      <h2>CONTACT</h2>
      <a
        class="insta-link"
        href="https://www.instagram.com/francescabmccormick/?hl=en"
        target="_blank"
      >
        <font-awesome-icon :icon="['fab', 'instagram']" />
        Instagram
      </a>
    </div>
    <div class="form-container">
      <form @submit.prevent="sendEmail">
        <input
          id="name"
          v-model="name"
          class="form-group"
          type="text"
          name="name"
          placeholder="Name"
        >
        <input
          id="email"
          v-model="email"
          class="form-group"
          name="email"
          type="email"
          placeholder="Email"
        >
        <textarea
          id="message"
          v-model="message"
          class="form-group form-group-textarea"
          name="message"
          placeholder="Add a message"
        />
        <button class="submit-button" type="submit" value="Send">
          Submit
        </button>
      </form>
    </div>
  </section>
</template>

<script>
import { sendForm } from 'emailjs-com'

export default {
  data () {
    return {
      name: '',
      email: '',
      message: ''
    }
  },
  methods: {
    sendEmail (e) {
      try {
        sendForm(
          'service_i53z8am',
          'template_atl4edp',
          e.target,
          'user_12FyiUAE9iIeOxJijTOfS',
          {
            name: this.name,
            email: this.email,
            message: this.message
          }
        )
      } catch (error) {
        console.log({ error })
      }
      this.name = ''
      this.email = ''
      this.message = ''
    }
  }
}
</script>

<style lang="scss" scoped>
/* Contact Page */

.insta-link {
  text-decoration: none;
  background-color: #ad2a67;
  color: white;
  padding: 1.3rem;
  border: 3px solid #2e3138;
  border-radius: 4px;
  margin-right: 2.5rem;

  &:hover {
    background-color: white;
    color: #ad2a67;
  }
}

.form-container {
  display: flex;
  justify-content: center;
  align-items: center;
}

form {
  padding: 2rem;
  width: 80%;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #2e3138;
  border-radius: 4px;
}

.form-group {
  max-width: 100%;
  width: 100%;
  height: 3.125rem;
  background-color: white;
  border: 3px solid #ad2a67;
  border-radius: 4px;
  margin-bottom: 1.5rem;
  padding-left: 0.5rem;
  font-size: 1rem;
  font-family: "Open Sans", Arial, Helvetica, sans-serif;

  &:hover {
    background-color: #fad0c6;
  }
}

.form-group-textarea {
  height: 6.25rem;
  padding-top: 0.75rem;
}

.submit-button {
  height: 3.125rem;
  width: 50%;
  background-color: #ad2a67;
  color: white;
  border: 3px solid white;
  border-radius: 4px;
  margin: 0 auto;
  cursor: pointer;
  font-size: 1rem;

  &:hover {
    background-color: white;
    color: #ad2a67;
  }
}

@media screen and (max-width: 900px) {
  .insta-link {
    margin-right: 0;
    padding: 0.81rem;
  }
}
</style>
