<template>
    <div class="card" :class="{ 'card-hover': isHovered }" @mouseover="isHovered = true" @mouseleave="isHovered = false">
      <img :src="image" alt="Card Image" class="card-image">
      <div class="card-content">
        <h3 class="card-title">{{ title }}</h3>
        <div class="card-description" v-show="isHovered">{{ description }}</div>
      </div>
      <div class="card-buttons">
        <a v-for="(button, index) in buttons" :key="index" :href="button.url" class="card-button">
          {{ button.label }}
        </a>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      image: {
        type: String,
        default: 'default-image.jpg'
      },
      title: {
        type: String,
        default: 'Título de la carta'
      },
      description: {
        type: String,
        default: 'Descripción de la carta'
      },
      buttons: {
        type: Array,
        default: () => [
          { label: 'Botón 1', url: '#' },
          { label: 'Botón 2', url: '#' }
        ]
      }
    },
    data() {
      return {
        isHovered: false
      };
    }
  };
  </script>
  
  <style scoped>
  .card {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 500px;
    height: 500px;
    padding: 20px;
    border: 5px solid #c70039;
    font-size: 16px;
    font-family: 'Montserrat', sans-serif;
    border-radius: 10px;
    transition: transform 0.5s ease;
  }
  
  .card-hover {
    transform: scale(1.1);
    transition: transform 0.8s ease;
  }
  
  .card-image {
    width: 70%;
    height: 55%;
    margin-bottom: 10px;
  }
  
  .card-content {
    margin-top: 5%;
    text-align: center;
  }
  
  .card-title {
    margin-bottom: 10px;
  }
  
  .card-description {
    margin-bottom: 10px;
  }
  
  .card-buttons {
    display: flex;
  }
  
  .card-button {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 50px;
    height: 50px;
    margin-right: 5px;
    border-radius: 50%;
    background-color: #c70039;
    color: black;
    text-decoration: none;
    font-size: 24px;
    font-family: 'Montserrat', sans-serif;
  }
  </style>
  