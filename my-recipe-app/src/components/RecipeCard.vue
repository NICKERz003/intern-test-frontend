<template>
  <div class="card">
    <div class="image-wrapper">
      <img :src="image" :alt="title" />
      <div class="overlay">
        <h3 class="card-title">{{ title }}</h3>
        <p class="card-info">{{ time }} | {{ servings }} servings</p>
      </div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  title: String,
  time: String,
  servings: Number,
  image: String
})
</script>

<style scoped>
.card {
  background: white;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
  transition: transform 0.3s ease;
  cursor: pointer;
}

.card:hover {
  transform: translateY(-5px);
}

.image-wrapper {
  position: relative;
  height: 300px; /* ความสูงของการ์ด */
}

.image-wrapper img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  padding: 20px;
  background: linear-gradient(transparent, rgba(0,0,0,0.8));
  color: white;
}

.card-title {
  font-size: 1.1rem;
  font-weight: bold;
  text-transform: uppercase;
  margin-bottom: 4px;
}

.card-info {
  font-size: 0.85rem;
  opacity: 0.8;
}
</style>