<script setup>
defineProps({ programs: Array })
</script>

<template>
  <section id="programs" class="section bg-light">
    <div class="container">
      <div class="section-header">
        <span class="section-tag">ACADEMIC OFFERINGS</span>
        <h2>Degree Programs Offered</h2>
        <div class="divider"></div>
      </div>

      <div class="grid-4">
        <div v-for="prog in programs" :key="prog.code" class="program-card">
          <div class="card-header">
            <span class="badge">{{ prog.badge }}</span>
            <h3 class="code">{{ prog.code }}</h3>
          </div>
          <div class="card-body">
            <h4 class="title">{{ prog.title }}</h4>
            <p class="desc">{{ prog.desc }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.section { padding: 80px 0; }
.bg-light { background-color: #f4f7f9; }
.container { max-width: 1200px; margin: 0 auto; padding: 0 20px; }

.section-header { text-align: center; margin-bottom: 50px; }
.section-tag { color: #002147; font-weight: 800; font-size: 0.8rem; letter-spacing: 2px; }
.section-header h2 { font-size: 2.25rem; font-weight: 900; color: #002147; margin-top: 5px; }
.divider { width: 60px; height: 4px; background-color: #f2c94c; margin: 15px auto 0; }

.grid-4 {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 25px;
}

.program-card {
  background-color: #ffffff;
  border-top: 4px solid #002147;
  border-radius: 8px;
  box-shadow: 0 4px 15px rgba(0,0,0,0.05);
  padding: 25px;
  transition: transform 0.2s, box-shadow 0.2s;
}

.program-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(0,0,0,0.1);
  border-top-color: #f2c94c;
}

.badge {
  display: inline-block;
  background-color: #fff8e1;
  color: #8c6b00;
  border: 1px solid #ffe082;
  font-size: 0.7rem;
  font-weight: 700;
  padding: 4px 10px;
  border-radius: 4px;
  margin-bottom: 12px;
}

.code {
  font-size: 2rem;
  font-weight: 900;
  color: #002147;
}

.title {
  font-size: 1rem;
  font-weight: 700;
  color: #1e293b;
  margin: 10px 0;
}

.desc {
  font-size: 0.88rem;
  color: #64748b;
  line-height: 1.6;
}
</style>