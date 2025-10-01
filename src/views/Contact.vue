<template>
  <section class="contact-page">
    <h1>Contact Us</h1>
    <p>We’d love to hear from you. Fill out the form below and we’ll get back to you soon.</p>

    <div class="card">
      <form @submit.prevent="handleSubmit">
        <div class="form-group">
          <label for="name">Full Name</label>
          <input type="text" id="name" v-model="form.name" required />
        </div>

        <div class="form-group">
          <label for="email">Email Address</label>
          <input type="email" id="email" v-model="form.email" required />
        </div>

        <div class="form-group">
          <label for="subject">Subject</label>
          <input type="text" id="subject" v-model="form.subject" required />
        </div>

        <div class="form-group">
          <label for="message">Message</label>
          <textarea id="message" rows="5" v-model="form.message" required></textarea>
        </div>

        <button type="submit" class="submit-btn">Send Message</button>
      </form>
    </div>
  </section>
</template>

<script>
export default {
  name: "Contact",
  data() {
    return {
      form: {
        name: "",
        email: "",
        subject: "",
        message: ""
      }
    }
  },
  methods: {
    handleSubmit() {
      // For now, just log the form data
      console.log("Form Submitted:", this.form)

      alert("Thank you! Your message has been sent.")
      this.form = { name: "", email: "", subject: "", message: "" }
    }
  }
}
</script>

<style scoped>
.contact-page {
  max-width: 800px;
  margin: auto;
  padding: 30px 20px;
  font-family: Arial, sans-serif;
}

h1 {
  text-align: center;
  margin-bottom: 10px;
  color: #222;
}

p {
  text-align: center;
  margin-bottom: 30px;
  color: #555;
}

.card {
  background: white;
  padding: 30px;
  border-radius: 10px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.form-group {
  margin-bottom: 20px;
}

label {
  display: block;
  font-weight: bold;
  margin-bottom: 8px;
  color: #333;
}

input,
textarea {
  width: 100%;
  padding: 12px;
  border: 1px solid #ddd;
  border-radius: 6px;
  font-size: 15px;
  outline: none;
}

input:focus,
textarea:focus {
  border-color: #42b983;
}

.submit-btn {
  background: #42b983;
  color: white;
  border: none;
  padding: 14px 20px;
  font-size: 16px;
  font-weight: bold;
  border-radius: 6px;
  cursor: pointer;
  transition: background 0.3s ease;
}

.submit-btn:hover {
  background: #368f6e;
}
</style>
