<script setup>
import { ref } from 'vue'
defineProps({ departments: Array })
const activeTab = ref(0)
</script>

<template>
  <section id="faculty" class="section">
    <div class="container">
      <div class="section-header">
        <span class="section-tag">OUR MENTORS</span>
        <h2>Faculty & Staff Directory</h2>
        <div class="divider"></div>
      </div>

      <!-- Department Tabs -->
      <div class="tabs">
        <button 
          v-for="(dept, index) in departments" 
          :key="dept.name"
          @click="activeTab = index"
          :class="['tab-btn', { active: activeTab === index }]">
          {{ dept.name }}
        </button>
      </div>

      <!-- Faculty List with Ordered Number Circle Badges -->
      <div class="faculty-grid">
        <div v-for="person in departments[activeTab].members" :key="person.id" class="faculty-card">
          <div class="number-circle">
            #{{ person.id }}
          </div>
          <div class="faculty-details">
            <h3 class="name">{{ person.name }}</h3>
            <p class="degree">{{ person.degree }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.section { padding: 80px 0; background-color: #ffffff; }
.container { max-width: 1200px; margin: 0 auto; padding: 0 20px; }

.section-header { text-align: center; margin-bottom: 40px; }
.section-tag { color: #002147; font-weight: 800; font-size: 0.8rem; letter-spacing: 2px; }
.section-header h2 { font-size: 2.25rem; font-weight: 900; color: #002147; margin-top: 5px; }
.divider { width: 60px; height: 4px; background-color: #f2c94c; margin: 15px auto 0; }

.tabs {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 10px;
  margin-bottom: 40px;
}

.tab-btn {
  background-color: #e2e8f0;
  border: none;
  padding: 10px 22px;
  border-radius: 6px;
  font-weight: 700;
  color: #334155;
  cursor: pointer;
  transition: all 0.2s;
  font-size: 0.85rem;
}

.tab-btn.active {
  background-color: #002147;
  color: #f2c94c;
}

.faculty-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 20px;
}

.faculty-card {
  background-color: #f8fafc;
  border: 1px solid #e2e8f0;
  border-left: 5px solid #002147;
  border-radius: 8px;
  padding: 20px;
  display: flex;
  align-items: center;
  gap: 20px;
  transition: transform 0.2s;
}

.faculty-card:hover {
  transform: translateX(4px);
  border-left-color: #f2c94c;
}

/* Sequential Ordered Number Circle Badge */
.number-circle {
  width: 55px;
  height: 55px;
  min-width: 55px;
  border-radius: 50%;
  background-color: #002147;
  color: #f2c94c;
  font-size: 1.25rem;
  font-weight: 900;
  display: flex;
  align-items: center;
  justify-content: center;
  border: 2px solid #f2c94c;
}

.name {
  font-size: 1.1rem;
  font-weight: 800;
  color: #002147;
}

.degree {
  font-size: 0.85rem;
  color: #2563eb;
  font-weight: 600;
  margin-top: 4px;
}
</style>