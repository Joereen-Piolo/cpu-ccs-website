<script setup>
defineProps({ partners: Array })
</script>

<template>
  <section id="partnerships" class="section bg-navy text-white">
    <div class="container">
      <div class="section-header">
        <span class="section-tag light">GLOBAL NETWORKS</span>
        <h2 class="light">Partnerships & Memberships</h2>
        <div class="divider"></div>
      </div>

      <div class="partner-grid">
        <div v-for="partner in partners" :key="partner.name" class="partner-card">
          <div class="check-box">✓</div>
          <div>
            <h3>{{ partner.name }}</h3>
            <p>{{ partner.type }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.section { padding: 80px 0; }
.bg-navy { background-color: #00152e; }
.text-white { color: white; }
.container { max-width: 1200px; margin: 0 auto; padding: 0 20px; }

.section-header { text-align: center; margin-bottom: 50px; }
.section-tag.light { color: #f2c94c; font-weight: 800; font-size: 0.8rem; letter-spacing: 2px; }
.section-header h2.light { font-size: 2.25rem; font-weight: 900; color: #ffffff; margin-top: 5px; }
.divider { width: 60px; height: 4px; background-color: #f2c94c; margin: 15px auto 0; }

.partner-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
}

.partner-card {
  background-color: #002147;
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 8px;
  padding: 20px;
  display: flex;
  align-items: center;
  gap: 15px;
}

.check-box {
  width: 40px;
  height: 40px;
  min-width: 40px;
  background-color: #f2c94c;
  color: #002147;
  border-radius: 6px;
  font-weight: 900;
  display: flex;
  align-items: center;
  justify-content: center;
}

.partner-card h3 {
  font-size: 1rem;
  font-weight: 800;
  color: #ffffff;
}

.partner-card p {
  font-size: 0.8rem;
  color: #94a3b8;
  margin-top: 2px;
}
</style>