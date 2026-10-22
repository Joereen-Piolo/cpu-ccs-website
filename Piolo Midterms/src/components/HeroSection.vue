<template>
  <section id="hero" class="hero">
    <div class="hero-overlay">
      <div class="container hero-container">
        <div class="hero-badge">SCIENTIA ET FIDES</div>
        <h1>COLLEGE OF COMPUTER STUDIES</h1>
        <p class="hero-subtext">
          Excellence in Information Technology Education — Educating students with Christian principles and preparing them for lifetime learning and innovation.
        </p>
        <div class="hero-buttons">
          <a href="#programs" class="btn-gold">OUR ACADEMIC PROGRAMS</a>
          <a href="#faculty" class="btn-outline">MEET THE FACULTY</a>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero {
  background: linear-gradient(135deg, #00152e 0%, #002147 50%, #003366 100%);
  color: white;
  position: relative;
  text-align: center;
  border-bottom: 5px solid #f2c94c;
}

.hero-overlay {
  padding: 100px 20px;
  background: radial-gradient(circle, rgba(242,201,76,0.08) 0%, rgba(0,0,0,0) 70%);
}

.container {
  max-width: 900px;
  margin: 0 auto;
}

.hero-badge {
  display: inline-block;
  background-color: rgba(242, 201, 76, 0.2);
  color: #f2c94c;
  border: 1px solid #f2c94c;
  padding: 6px 16px;
  border-radius: 20px;
  font-size: 0.8rem;
  font-weight: 800;
  letter-spacing: 2px;
  margin-bottom: 20px;
}

h1 {
  font-size: 3rem;
  font-weight: 900;
  letter-spacing: 1px;
  margin-bottom: 20px;
  color: #ffffff;
}

.hero-subtext {
  font-size: 1.15rem;
  color: #e2e8f0;
  line-height: 1.7;
  margin-bottom: 35px;
}

.hero-buttons {
  display: flex;
  justify-content: center;
  gap: 15px;
  flex-wrap: wrap;
}

.btn-gold {
  background-color: #f2c94c;
  color: #002147;
  font-weight: 800;
  padding: 14px 28px;
  border-radius: 6px;
  text-decoration: none;
  font-size: 0.9rem;
  transition: all 0.2s;
}

.btn-gold:hover {
  background-color: #e0b430;
  transform: translateY(-2px);
}

.btn-outline {
  border: 2px solid #ffffff;
  color: #ffffff;
  font-weight: 800;
  padding: 12px 28px;
  border-radius: 6px;
  text-decoration: none;
  font-size: 0.9rem;
  transition: all 0.2s;
}

.btn-outline:hover {
  background-color: #ffffff;
  color: #002147;
}

@media (max-width: 768px) {
  h1 { font-size: 2rem; }
  .hero-subtext { font-size: 0.95rem; }
}
</style>