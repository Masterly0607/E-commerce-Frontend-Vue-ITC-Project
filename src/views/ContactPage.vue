<template>
  <div class="contact-page">
    <!-- Breadcrumb -->
    <div class="breadcrumb">
      Home / <span class="active">Contact</span>
    </div>

    <!-- Contact Section -->
    <div class="contact-container">
      
      <!-- Left Contact Info -->
      <div class="contact-info">
        <div class="info-box">
          <div class="icon">
            📞
          </div>
          <div class="info-text">
            <h3>Call To Us</h3>
            <p>We are available 24/7, 7 days a week.</p>
            <p>Phone: +8801611112222</p>
          </div>
        </div>

        <hr>

        <div class="info-box">
          <div class="icon">
            ✉️
          </div>
          <div class="info-text">
            <h3>Write To Us</h3>
            <p>Fill out our form and we will contact you within 24 hours.</p>
            <p>Emails: customer@exclusive.com</p>
            <p>support@exclusive.com</p>
          </div>
        </div>
      </div>

      <!-- Right Contact Form -->
      <div class="contact-form">
        <form @submit.prevent="submitForm">
          <div class="form-row">
            <input type="text" placeholder="Your Name *" v-model="form.name" required />
            <input type="email" placeholder="Your Email *" v-model="form.email" required />
            <input type="text" placeholder="Your Phone *" v-model="form.phone" required />
          </div>
          <div class="form-group">
            <textarea placeholder="Your Message" v-model="form.message" required></textarea>
          </div>
          <div class="form-submit">
            <button type="submit">Send Message</button>
          </div>
        </form>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'ContactPage',
  data() {
    return {
      form: {
        name: '',
        email: '',
        phone: '',
        message: ''
      }
    };
  },
  methods: {
    submitForm() {
      console.log('Form submitted:', this.form);
      alert("Message sent successfully!");
      this.form = {
        name: '',
        email: '',
        phone: '',
        message: ''
      };
    }
  }
};
</script>

<style scoped>
.contact-page {
  max-width: 1200px;
  margin: 50px auto;
  padding: 0 20px;
  font-family: Arial, sans-serif;
}

.breadcrumb {
  margin-bottom: 30px;
  color: #666;
  font-size: 16px;
}
.breadcrumb .active {
  color: #f7c600;
  font-weight: bold;
}

.contact-container {
  display: flex;
  justify-content: space-between;
  gap: 30px;
}

.contact-info, .contact-form {
  background: #fff;
  padding: 30px;
  border: 1px solid #eee;
  border-radius: 8px;
  width: 48%;
}

.info-box {
  display: flex;
  align-items: flex-start;
  gap: 15px;
  margin-bottom: 20px;
}

.icon {
  font-size: 30px;
  background: #f7c600;
  color: white;
  padding: 15px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.info-text h3 {
  margin: 0 0 5px 0;
  font-size: 18px;
}
.info-text p {
  margin: 5px 0;
  color: #666;
  font-size: 14px;
}

hr {
  border: 0;
  border-top: 1px solid #eee;
  margin: 20px 0;
}

.contact-form form {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

.form-row {
  display: flex;
  gap: 15px;
}

.form-row input {
  flex: 1;
  padding: 10px;
  border: 1px solid #ddd;
  border-radius: 4px;
  font-size: 14px;
  background: #f9f9f9;
}

.form-group textarea {
  width: 100%;
  padding: 10px;
  height: 150px;
  border: 1px solid #ddd;
  border-radius: 4px;
  font-size: 14px;
  background: #f9f9f9;
  resize: vertical;
}

.form-submit {
  text-align: right;
}

.form-submit button {
  background-color: #f7c600;
  border: none;
  padding: 10px 20px;
  color: white;
  font-weight: bold;
  font-size: 14px;
  border-radius: 4px;
  cursor: pointer;
}

.form-submit button:hover {
  background-color: #e6b800;
}

/* Responsive */
@media (max-width: 768px) {
  .contact-container {
    flex-direction: column;
  }

  .contact-info, .contact-form {
    width: 100%;
  }

  .form-row {
    flex-direction: column;
  }
}
</style>