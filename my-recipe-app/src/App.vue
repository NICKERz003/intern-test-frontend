<template>
  <div class="app-container">
    <header class="header-section">
      <h1 class="header-recommended">Recommended</h1>
      <h2 class="header-recipes">Recipes</h2>
    </header>

    <div class="recipe-grid">
      <RecipeCard
        v-for="(item, index) in recipeList"
        :key="index"
        v-bind="item"
      />
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import RecipeCard from "./components/RecipeCard.vue";

const recipeList = ref([
  {
    title: "Thang Noodle",
    time: "20 mins",
    servings: 4,
    image: "https://images.unsplash.com/photo-1552611052-33e04de081de?w=400",
  },
  {
    title: "Mango Sticky Rice",
    time: "25 mins",
    servings: 4,
    image:
      "https://delishglobe.com/wp-content/uploads/2024/10/Khao-Niew-Mamuang-Mango-Sticky-Rice-2048x1499.png",
  },
  {
    title: "Corn Spicy Salad",
    time: "10 mins",
    servings: 2,
    image: "https://images.unsplash.com/photo-1546069901-ba9599a7e63c?w=400",
  },
  {
    title: "Thang Noodle",
    time: "20 mins",
    servings: 4,
    image: "https://images.unsplash.com/photo-1569718212165-3a8278d5f624?w=400",
  },
  {
    title: "Mango Sticky Rice",
    time: "25 mins",
    servings: 4,
    image: "https://delishglobe.com/wp-content/uploads/2024/10/Khao-Niew-Mamuang-Mango-Sticky-Rice-2048x1499.png",
  },
  {
    title: "Corn Spicy Salad",
    time: "10 mins",
    servings: 2,
    image: "https://images.unsplash.com/photo-1546069901-ba9599a7e63c?w=400",
  },
]);
</script>
