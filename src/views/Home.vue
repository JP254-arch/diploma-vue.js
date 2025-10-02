<template>
  <div class="home-page">
    <!-- Full-width Hero Image -->
    <img src="/images/home 1.png" alt="Car Hero" class="hero-img" />

    <!-- Heading + Hero Content -->
    <h1>{{ heroTitle }}</h1>
    <section class="hero">
      <div class="hero-content">
        <p>{{ heroSubtitle }}</p>
        <button class="cta-btn">{{ heroButton }}</button>
      </div>
    </section>

    <!-- About Preview -->
    <section class="about-preview">
      <div class="text">
        <h2>About Us</h2>
        <p>{{ aboutPreview }}</p>
        <router-link to="/about" class="learn-more">Learn More →</router-link>
      </div>
    </section>

    <!-- Core Values -->
    <section class="values">
      <h2>Our Core Values</h2>
      <div class="value-grid">
        <div v-for="(value, i) in values" :key="i" class="value-card">
          <img :src="value.image" :alt="value.title" />
          <h3>{{ value.title }}</h3>
        </div>
      </div>
    </section>

    <!-- Services Section -->
    <section class="services">
      <h2>Our Services</h2>
      <div class="service-list">
        <div v-for="(service, i) in services" :key="i" class="service-card">
          <h3>{{ service.title }}</h3>
          <p>{{ service.text }}</p>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
  export default {
    name: "Home",
    data() {
      return {
        heroTitle: "Welcome to MotorHub",
        heroSubtitle: "Your trusted car dealership for quality new & used vehicles.",
        heroButton: "Explore Vehicles",

        aboutPreview: `At MotorHub Limited, we pride ourselves on delivering top-quality
        vehicles, whether brand-new or pre-owned. With years of trusted
        experience in importation and sales, we connect our customers to
        reliable cars that match their needs and lifestyle.`,

        values: [
          { title: "Reliability", image: "/images/reliability.png" },
          { title: "Integrity", image: "/images/integrity.png" },
          { title: "Customer Service", image: "/images/customer -service.png" },
          { title: "Satisfaction", image: "/images/customer-satisfaction.png" }
        ],

        services: [
          {
            title: "Vehicle Sales",
            text: "Brand new, foreign used, and locally used vehicles for individuals and corporates."
          },
          {
            title: "Imports on Behalf",
            text: "Hassle-free importation of your dream vehicle from trusted global markets."
          },
          {
            title: "Service Center",
            text: "Maintenance, respray, panel beating, upgrades, parts, and accessories."
          }
        ]
      };
    }
  };
</script>

<style scoped>
  h1 {
    color: rgb(239, 46, 3);
    text-align: center;
    margin: 30px 0 20px;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  }

  .home-page {
    font-family: Arial, sans-serif;
    color: #333;
  }

  /* Full-width Hero Image */
  .hero-img {
    width: 100%;
    height: 400px;
    object-fit: cover;
    display: block;
  }

  /* Hero Section */
  .hero {
    text-align: center;
    padding: 40px 20px;
  }

  .hero-content p {
    font-size: 1.2rem;
    margin-bottom: 20px;
    color: #555;
  }

  .cta-btn {
    background: #f00869;
    color: white;
    border: none;
    padding: 14px 24px;
    font-size: 16px;
    border-radius: 6px;
    cursor: pointer;
  }

  .cta-btn:hover {
    background: #368f6e;
  }

  /* About Preview */
  .about-preview {
    display: flex;
    align-items: center;
    padding: 60px 20px;
    gap: 40px;
  }

  .learn-more {
    display: inline-block;
    margin-top: 10px;
    color: #42b983;
    font-weight: bold;
  }

  /* Values */
  .values {
    padding: 60px 20px;
    text-align: center;
    color: rgb(255, 85, 0);
  }

  .value-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 30px;
    margin-top: 30px;
  }

  .value-card {
    background: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
  }

  .value-card img {
    max-width: 80px;
    margin-bottom: 15px;
  }

  /* Services */
  .services {
    padding: 60px 20px;
    background: #f1f1f1;
    text-align: center;
  }

  .service-list {
    display: flex;
    gap: 30px;
    justify-content: center;
    flex-wrap: wrap;
    margin-top: 30px;
  }

  .service-card {
    background: white;
    padding: 40px;
    border-radius: 10px;
    max-width: 300px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
  }

  .service-card h3 {
    margin-bottom: 10px;
    color: #d43a34;
  }

  /* Responsive */
  @media (max-width: 768px) {
    .about-preview {
      flex-direction: column;
      text-align: center;
    }

    .hero-img {
      height: 250px;
    }
  }
</style>
