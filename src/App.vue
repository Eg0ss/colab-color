<script setup>
import Colors from './components/Colors.vue';

const colors = [
    {
        id: 1,
        name: "Red",
        hex: "#FF0000",
        rgb: "rgb(255, 0, 0)",
        hsl: "hsl(0, 100%, 50%)",
        category: "primary"
    },
    {
        id: 2,
        name: "Blue",
        hex: "#0000FF",
        rgb: "rgb(0, 0, 255)",
        hsl: "hsl(240, 100%, 50%)",
        category: "primary"
    },
    {
        id: 3,
        name: "Green",
        hex: "#008000",
        rgb: "rgb(0, 128, 0)",
        hsl: "hsl(120, 100%, 25%)",
        category: "primary"
    },
    {
        id: 4,
        name: "Yellow",
        hex: "#FFFF00",
        rgb: "rgb(255, 255, 0)",
        hsl: "hsl(60, 100%, 50%)",
        category: "secondary"
    },
    {
        id: 5,
        name: "Cyan",
        hex: "#00FFFF",
        rgb: "rgb(0, 255, 255)",
        hsl: "hsl(180, 100%, 50%)",
        category: "secondary"
    },
    {
        id: 6,
        name: "Magenta",
        hex: "#FF00FF",
        rgb: "rgb(255, 0, 255)",
        hsl: "hsl(300, 100%, 50%)",
        category: "secondary"
    },
    {
        id: 7,
        name: "Orange",
        hex: "#FFA500",
        rgb: "rgb(255, 165, 0)",
        hsl: "hsl(39, 100%, 50%)",
        category: "warm"
    },
    {
        id: 8,
        name: "Purple",
        hex: "#800080",
        rgb: "rgb(128, 0, 128)",
        hsl: "hsl(300, 100%, 25%)",
        category: "cool"
    },
    {
        id: 9,
        name: "Pink",
        hex: "#FFC0CB",
        rgb: "rgb(255, 192, 203)",
        hsl: "hsl(350, 100%, 88%)",
        category: "warm"
    },
    {
        id: 10,
        name: "Brown",
        hex: "#8B4513",
        rgb: "rgb(139, 69, 19)",
        hsl: "hsl(25, 76%, 31%)",
        category: "earth"
    },
    {
        id: 11,
        name: "Black",
        hex: "#000000",
        rgb: "rgb(0, 0, 0)",
        hsl: "hsl(0, 0%, 0%)",
        category: "neutral"
    },
    {
        id: 12,
        name: "White",
        hex: "#FFFFFF",
        rgb: "rgb(255, 255, 255)",
        hsl: "hsl(0, 0%, 100%)",
        category: "neutral"
    },
    {
        id: 13,
        name: "Gray",
        hex: "#808080",
        rgb: "rgb(128, 128, 128)",
        hsl: "hsl(0, 0%, 50%)",
        category: "neutral"
    },
    {
        id: 14,
        name: "Teal",
        hex: "#008080",
        rgb: "rgb(0, 128, 128)",
        hsl: "hsl(180, 100%, 25%)",
        category: "cool"
    },
    {
        id: 15,
        name: "Lime",
        hex: "#00FF00",
        rgb: "rgb(0, 255, 0)",
        hsl: "hsl(120, 100%, 50%)",
        category: "cool"
    },
    {
        id: 16,
        name: "Indigo",
        hex: "#4B0082",
        rgb: "rgb(75, 0, 130)",
        hsl: "hsl(275, 100%, 25%)",
        category: "cool"
    },
    {
        id: 17,
        name: "Gold",
        hex: "#FFD700",
        rgb: "rgb(255, 215, 0)",
        hsl: "hsl(51, 100%, 50%)",
        category: "warm"
    },
    {
        id: 18,
        name: "Coral",
        hex: "#FF7F50",
        rgb: "rgb(255, 127, 80)",
        hsl: "hsl(16, 100%, 66%)",
        category: "warm"
    },
    {
        id: 19,
        name: "Turquoise",
        hex: "#40E0D0",
        rgb: "rgb(64, 224, 208)",
        hsl: "hsl(174, 72%, 56%)",
        category: "cool"
    },
    {
        id: 20,
        name: "Violet",
        hex: "#EE82EE",
        rgb: "rgb(238, 130, 238)",
        hsl: "hsl(300, 76%, 72%)",
        category: "cool"
    }
]

</script>

<template>
  <div class="page-wrapper">
    <section class="hero-header">
      <div class="hero-content">
        <span class="top-badge">Configurateur Visuel</span>
        <h1>Personnalisez votre <span>Interface</span></h1>
        <p>Sélectionnez une nuance dans notre palette exclusive pour définir l'identité de votre portail employé.</p>
      </div>
    </section>

    <section class="picker-section">
      <div class="section-title">
        <h2>Palette de Couleurs</h2>
        <div class="divider"></div>
      </div>
      
      <div class="colors-container">
        <Colors :colors="colors" />
      </div>
    </section>
  </div>
</template>

<style scoped>
.page-wrapper {
  background-color: #ffffff;
  min-height: 100vh;
}

.hero-header {
  background: linear-gradient(135deg, #0f172a 0%, #0c4a6e 100%);
  padding: 100px 20px;
  text-align: center;
  color: white;
  clip-path: polygon(0 0, 100% 0, 100% 90%, 0% 100%); 
}

.hero-content {
  max-width: 800px;
  margin: 0 auto;
}

.top-badge {
  background: #0ea5e9;
  color: white;
  padding: 5px 15px;
  border-radius: 4px;
  font-weight: 800;
  font-size: 0.75rem;
  text-transform: uppercase;
  letter-spacing: 2px;
  display: inline-block;
  margin-bottom: 20px;
}

h1 {
  font-size: 3.5rem;
  font-weight: 900;
  margin-bottom: 20px;
  line-height: 1.1;
}

h1 span {
  color: #0ea5e9;
}

.hero-header p {
  font-size: 1.1rem;
  color: #bae6fd;
  max-width: 600px;
  margin: 0 auto;
  line-height: 1.6;
}

.picker-section {
  max-width: 1200px;
  margin: -50px auto 100px;
  padding: 60px 40px;
  background: white;
  border-radius: 12px;
  box-shadow: 0 30px 60px rgba(0,0,0,0.12);
  position: relative;
  z-index: 10;
}

.section-title {
  margin-bottom: 40px;
  text-align: left;
}

.section-title h2 {
  font-size: 1.8rem;
  font-weight: 800;
  color: #1e293b;
  margin-bottom: 10px;
}

.divider {
  width: 60px;
  height: 4px;
  background: #0ea5e9;
  border-radius: 2px;
}

.colors-container {
  display: block;
}

.page-wrapper {
  animation: fadeIn 0.8s ease-out;
}

@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

@media (max-width: 768px) {
  h1 { font-size: 2.2rem; }
  .hero-header { padding: 60px 20px 80px; }
  .picker-section { margin: -30px 15px 50px; padding: 30px 20px; }
}
</style>