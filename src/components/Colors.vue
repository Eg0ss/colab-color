<script setup>
import { ref } from 'vue';
import Color from './Color.vue';

const currentColor = ref('')

const props = defineProps({
    colors: Array
})
console.log(props.colors);

function display(color){
  currentColor.value = color.rgb;
}

</script>

<template>
    <div class="color-picker-container">
        <h3 class="picker-title">Personnalisation du thème</h3>
        
        <div class="colors-grid">
            <span v-for="color in colors" :key="color.id" @click="display(color)" class="color-wrapper">
                <Color :color="color"></Color>
            </span>
        </div>

        <div class="preview-box" :style="{ borderLeftColor: currentColor }">
            <div class="color-swatch" :style="{ backgroundColor: currentColor }"></div>
            <div class="preview-text">
                <p class="label">Couleur sélectionnée</p>
                <p class="hex-value">{{ currentColor || 'Aucune' }}</p>
            </div>
        </div>
    </div>
</template>

<style scoped>
.color-picker-container {
    background: #ffffff;
    padding: 25px;
    border-radius: 12px;
    border: 1px solid #edf2f7;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
}

.picker-title {
    font-size: 0.9rem;
    font-weight: 800;
    text-transform: uppercase;
    color: #1a2942;
    letter-spacing: 1px;
    margin-bottom: 20px;
    border-left: 4px solid #0ea5e9;
    padding-left: 12px;
}

.colors-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    margin-bottom: 25px;
}

.color-wrapper {
    cursor: pointer;
    transition: transform 0.2s cubic-bezier(0.175, 0.885, 0.32, 1.275);
}

.color-wrapper:hover {
    transform: scale(1.15);
}

.preview-box {
    display: flex;
    align-items: center;
    gap: 15px;
    padding: 15px;
    background: #f8fafc;
    border-radius: 8px;
    border-left: 6px solid #e2e8f0; 
    transition: border-color 0.4s ease;
}

.color-swatch {
    width: 45px;
    height: 45px;
    border-radius: 6px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    border: 2px solid #ffffff;
}

.preview-text {
    display: flex;
    flex-direction: column;
}

.label {
    font-size: 0.75rem;
    font-weight: 700;
    color: #64748b;
    margin: 0;
    text-transform: uppercase;
}

.hex-value {
    font-size: 1.1rem;
    font-weight: 900;
    color: #1e293b;
    margin: 0;
    font-family: 'Monaco', monospace;
}
</style>
