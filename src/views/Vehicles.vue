<template>
  <section class="vehicles-page">
    <h2>Vehicles</h2>
    <p>Browse the MotorHub vehicle lineup.</p>

    <div class="vehicle-grid">
      <!-- Car 1 -->
      <div class="vehicle-card">
        <img src="/public/images/audi 1.jpg" alt="Car 1" class="vehicle-img" />
        <h3>Audi</h3>
        <p>2025 Model</p>
      </div>

      <!-- Car 2 -->
      <div class="vehicle-card">
        <img src="/public/images/audi 2.jpg" alt="Car 2" class="vehicle-img" />
        <h3>Audi</h3>
        <p>Sport</p>
      </div>

      <!-- Car 3 -->
      <div class="vehicle-card">
        <img src="/public/images/audi 3.jpg" alt="Car 3" class="vehicle-img" />
        <h3>Audi</h3>
        <p>Sprint</p>
      </div>

      <!-- Car 4 -->
      <div class="vehicle-card">
        <img src="/public/images/audi 4.jpg" alt="Car 4" class="vehicle-img" />
        <h3>Audi</h3>
        <p>Sport</p>
      </div>

      <!-- Car 5 -->
      <div class="vehicle-card">
        <img src="/public/images/home 1.png" alt="Car 5" class="vehicle-img" />
        <h3>Lexus</h3>
        <p>2025 Model</p>
      </div>

      <!-- Car 6 -->
      <div class="vehicle-card">
        <img src="/public/images/home 2.png" alt="Car 6" class="vehicle-img" />
        <h3>Range Rover</h3>
        <p>New Series</p>
      </div>

      <!-- Car 7 -->
      <div class="vehicle-card">
        <img src="/public/images/home 3.png" alt="Car 7" class="vehicle-img" />
        <h3>Mercedes</h3>
        <p>G - Class</p>
      </div>

      <!-- Car 8 -->
      <div class="vehicle-card">
        <img src="/public/images/home 4.jpg" alt="Car 8" class="vehicle-img" />
        <h3>Tesla</h3>
        <p>Dutch</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Vehicles",
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
  grid-template-columns: repeat(4, 1fr); /* 4 cards per row */
  gap: 20px;
  justify-items: center;
}

/* Vehicle Card */
.vehicle-card {
  background: #fff;
  border: 1px solid #ddd;
  border-radius: 8px;
  width: 100%;
  max-width: 260px; /* keep them consistent like table cells */
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
