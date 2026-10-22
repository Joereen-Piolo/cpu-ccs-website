<script setup>
defineProps({ navItems: Array })
</script>

<template>
  <header class="header-wrapper">
    <!-- Top Bar -->
    <div class="top-bar">
      <div class="container top-bar-content">
        <span>📍 Central Philippine University, Jaro, Iloilo City</span>
        <span>✉️ ccssec@cpu.edu.ph | 📞 (033) 329-1971</span>
      </div>
    </div>

    <!-- Main Navigation Bar -->
    <nav class="main-nav">
      <div class="container nav-content">
        <div class="brand">
          <div class="cpu-logo-badge">CPU</div>
          <div class="brand-text">
            <span class="college-title">COLLEGE OF COMPUTER STUDIES</span>
            <span class="sub-title">Central Philippine University</span>
          </div>
        </div>

        <ul class="nav-links">
          <li v-for="item in navItems" :key="item.name">
            <a :href="item.href">{{ item.name }}</a>
          </li>
        </ul>
      </div>
    </nav>
  </header>
</template>

<style scoped>
.header-wrapper {
  position: sticky;
  top: 0;
  z-index: 1000;
  box-shadow: 0 4px 12px rgba(0,0,0,0.15);
}

.top-bar {
  background-color: #00152e;
  color: #d1d5db;
  font-size: 0.8rem;
  padding: 6px 0;
  border-bottom: 1px solid rgba(255, 255, 255, 0.1);
}

.top-bar-content {
  display: flex;
  justify-content: space-between;
}

.main-nav {
  background-color: #002147; /* CPU Navy Blue */
  padding: 12px 0;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

.nav-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.brand {
  display: flex;
  align-items: center;
  gap: 12px;
}

.cpu-logo-badge {
  width: 45px;
  height: 45px;
  border-radius: 50%;
  background-color: #f2c94c; /* CPU Gold */
  color: #002147;
  font-weight: 900;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1rem;
  border: 2px solid white;
}

.brand-text {
  display: flex;
  flex-direction: column;
}

.college-title {
  color: #ffffff;
  font-weight: 800;
  font-size: 1.1rem;
  letter-spacing: 0.5px;
}

.sub-title {
  color: #f2c94c;
  font-size: 0.75rem;
  font-weight: 600;
}

.nav-links {
  display: flex;
  list-style: none;
  gap: 20px;
}

.nav-links a {
  color: #ffffff;
  text-decoration: none;
  font-size: 0.85rem;
  font-weight: 700;
  letter-spacing: 0.5px;
  padding: 8px 12px;
  border-radius: 4px;
  transition: all 0.2s;
}

.nav-links a:hover {
  background-color: #f2c94c;
  color: #002147;
}

@media (max-width: 768px) {
  .top-bar { display: none; }
  .nav-links { gap: 8px; }
  .nav-links a { font-size: 0.75rem; padding: 4px 6px; }
  .college-title { font-size: 0.9rem; }
}
</style>