<template>
  <section class="about-page">
    <!-- About Section -->
    <h1>ABOUT US</h1>
    <p>
      Motorhub Limited is a car dealership incorporated in Kenya dealing with importation and sale of new and
      second-hand Motor Vehicles. At Motorhub, we pride ourselves in offering quality and carefully sourced Vehicles,
      guided by our core values and a burning desire to satisfy customer needs. Vehicles in our dealership are sourced
      from Japan, Thailand, United Kingdom, Australia, South Africa and host of other countries to ensure variety of
      units to meet market demand.
    </p>

    <!-- Core Values -->
    <h2>CORE VALUES</h2>
    <table class="core-values">
      <tr>
        <td><b><i>Reliability</i></b></td>
        <td><b><i>Integrity</i></b></td>
        <td><b><i>Customer Service</i></b></td>
        <td><b><i>Customer Satisfaction</i></b></td>
      </tr>
      <tr>
        <td><img src="/public/images/reliability.png" alt="reliability" /></td>
        <td><img src="/public/images/integrity.png" alt="integrity" /></td>
        <td><img src="/public/images/customer -service.png" alt="customer service" /></td>
        <td><img src="/public/images/customer-satisfaction.png" alt="customer satisfaction" /></td>
      </tr>
    </table>

    <div class="center">
      <button class="contact-btn">GET IN TOUCH WITH US</button>
    </div>

    <!-- Mission & Vision -->
    <div class="container">
      <div class="row">
        <div class="column-66">
          <h1><b>OUR MISSION</b></h1>
          <p>To offer excellent customer satisfaction by providing affordable and top-of-the-range Motor Vehicles.</p>
          <h1><b>VISION</b></h1>
          <p>
            To be the number one dealer choice for individual and corporate buyers of Motor Vehicles in Kenya and
            beyond, as well as offering Motor vehicle advisory services and mechanical/technical support to all our
            customers.
          </p>
        </div>
        <div class="column-33">
          <img src="/public/images/mission.jpg" alt="mission" />
        </div>
      </div>
    </div>

    <!-- Services -->
    <div class="container alt">
      <div class="row">
        <div class="column-33">
          <img src="/public/images/services.jpg" alt="services" />
        </div>
        <div class="column-66">
          <h1 class="highlight">Clarity</h1>
          <h1><b>OUR SERVICES</b></h1>
          <ul>
            <li>
              Direct sale of brand new, foreign used and locally used Vehicles to both individuals and corporates.
            </li>
            <li>
              Imports on behalf - allowing customers to ship in their desired Vehicle without the hassle and logistical
              complexities involved.
            </li>
            <li>
              A service center offering Motor Vehicle maintenance services, such as respray, panel beating, upgrades,
              accessories and parts.
            </li>
          </ul>
        </div>
      </div>
    </div>

    <!-- Corporate Clients -->
    <div class="container">
      <div class="row">
        <div class="column-66">
          <h1><b>TAILORED SERVICES TO CORPORATE CLIENTS</b></h1>
          <ul>
            <li>Specialized partnership offers and discounts on bulk orders.</li>
            <li>
              A wide variety of Vehicle options for convenient transportation of staff, students and other corporate and
              company stakeholders.
            </li>
            <li>Convenience of Vehicle service and maintenance of a company's entire fleet under one roof.</li>
            <li>Aftermarket installation of special car parts and modification.</li>
            <li>High grade Vehicle branding and painting services.</li>
            <li>Importation of special service Vehicles on behalf e.g. Ambulance</li>
          </ul>
        </div>
        <div class="column-33">
          <img src="/public/images/clients.jpg" alt="clients" />
        </div>
      </div>
    </div>

    <!-- Bottom Image -->
    <!-- <img src="/contact-bottom.jpg" alt="contact" class="bottom-banner" /> -->

  </section>
</template>

<script>
export default {
  name: "About"
}
</script>

<style scoped>
.about-page {
  line-height: 1.6;
  font-family: Arial, sans-serif;
  color: #333;
}
h1{
    text-align: center;
}

h2 {
  margin-top: 20px;
  color: #111;
}

.core-values {
  width: 100%;
  text-align: center;
  margin: 20px 0;
}
.core-values td {
  padding: 10px;
}
.core-values img {
  width: 100px;
}

.center {
  text-align: center;
  margin: 20px 0;
}
.contact-btn {
  background: red;
  color: white;
  border: none;
  padding: 12px 24px;
  font-size: 16px;
  cursor: pointer;
  border-radius: 5px;
}
.contact-btn:hover {
  background: darkred;
}

.container {
  padding: 40px 20px;
}
.container.alt {
  background: #f1f1f1;
}
.row {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 20px;
}
.column-66 {
  flex: 2;
}
.column-33 {
  flex: 1;
}
.column-33 img,
.column-66 img {
  max-width: 100%;
  height: auto;
}

.highlight {
  color: red;
}

.bottom-banner {
  width: 100%;
  display: block;
  margin-top: 30px;
}
</style>
