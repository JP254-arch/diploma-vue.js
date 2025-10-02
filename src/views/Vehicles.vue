<template>
  <section class="vehicles-page">
    <h2>Vehicles</h2>
    <p>Browse the MotorHub vehicle lineup.</p>

    <div class="vehicle-grid">
      <div v-for="(vehicle, index) in vehicles" :key="index" class="vehicle-card">
        <img :src="vehicle.image" :alt="vehicle.name" class="vehicle-img" />
        <h3>{{ vehicle.name }}</h3>
        <p>{{ vehicle.model }}</p>
      </div>
    </div>
  </section>
</template>

<script>
  export default {
    name: "Vehicles",
    data() {
      return {
        vehicles: [
          {
            name: "Audi",
            model: "2025 Model",
            image: "/images/audi 1.jpg"
          },
          {
            name: "Audi",
            model: "Sport",
            image: "/images/audi 2.jpg"
          },
          {
            name: "Audi",
            model: "Sprint",
            image: "/images/audi 3.jpg"
          },
          {
            name: "Audi",
            model: "Sport",
            image: "/images/audi 4.jpg"
          },
          {
            name: "Lexus",
            model: "2025 Model",
            image: "/images/home 1.png"
          },
          {
            name: "Range Rover",
            model: "New Series",
            image: "/images/home 2.png"
          },
          {
            name: "Mercedes",
            model: "G - Class",
            image: "/images/home 3.png"
          },
          {
            name: "Tesla",
            model: "Dutch",
            image: "/images/home 4.jpg"
          },
          {
            name: "Tesla",
            model: "Dutch",
            image: "/images/home 4.jpg"
          },
          {
            name: "Volvo",
            model: "S - Class",
            image: "https://images.unsplash.com/photo-1671880399129-4d1ff944f2f3?w=800&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTJ8fHZlaGljbGVzfGVufDB8fDB8fHww"
          }
        ]
      };
    }
  };
</script>
<style scoped>
  .vehicles-page {
    padding: 40px 20px;
    text-align: center;
  }

  .vehicles-page h2 {
    font-size: 2.5rem;
    margin-bottom: 10px;
    color: #0365ef;
    font-weight: bold;
  }

  .vehicles-page p {
    margin-bottom: 30px;
    color: #555;
    font-size: 1.1rem;
  }

  /* Vehicle Grid - Table-like layout */
  .vehicle-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    /* 4 cards per row */
    gap: 20px;
    justify-items: center;
  }

  /* Vehicle Card */
  .vehicle-card {
    background: #fff;
    border: 1px solid #ddd;
    border-radius: 8px;
    width: 100%;
    max-width: 260px;
    /* keep them consistent like table cells */
    padding: 15px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
    text-align: center;
    transition: all 0.3s ease;
    padding: 9px;
  }

  .vehicle-card:hover {
    transform: translateY(-6px);
    box-shadow: 0 6px 14px rgba(0, 0, 0, 0.1);
  }

  .vehicle-img {
    width: 100%;
    height: 180px;
    object-fit: cover;
    border-radius: 6px;
    margin-bottom: 12px;
    background: #f2f2f2;
  }

  .vehicle-card h3 {
    font-size: 1.2rem;
    margin: 10px 0;
    color: #333;
  }

  .vehicle-card p {
    font-size: 0.95rem;
    color: #666;
  }

  /* Responsive breakpoints */
  @media (max-width: 1024px) {
    .vehicle-grid {
      grid-template-columns: repeat(3, 1fr);
    }
  }

  @media (max-width: 768px) {
    .vehicle-grid {
      grid-template-columns: repeat(2, 1fr);
    }
  }

  @media (max-width: 480px) {
    .vehicle-grid {
      grid-template-columns: 1fr;
    }
  }
</style>