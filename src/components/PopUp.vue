<script setup>
import { defineEmits } from "vue";

const emits = defineEmits(["close"]);
</script>

<template>
  <div class="popup">
    <div class="popup-content">
      <ul>
        <li>
          <a href="#">Home</a>
        </li>
        <li>
          <a href="#">Blog</a>
        </li>
        <li>
          <a href="#">Setup</a>
        </li>
      </ul>
      <button class="close-btn" @click="$emit('close')">Fechar</button>
    </div>
  </div>
</template>

<style scoped>
.popup {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background: rgba(129, 129, 129, 0.144);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}

.popup-content {
  display: flex;
  width: 200px;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  color: #ffffff;
  padding: 20px;
  border-radius: 10px;
  text-align: center;
  backdrop-filter: blur(4.5px);
  --webkit-backdrop-filter: blur(4.5px);
  --moz-backdrop-filter: blur(4.5px);
  background-color: rgba(221, 219, 219, 0.5);
}

.popup-content ul {
  all: none;
  list-style: none;
  padding: 0;
  font-size: 32px;
  font-family: "Gilroy", "Inter", sans-serif;
  font-weight: 700;
}

.popup-content ul li a {
  all: unset;
}

.popup-content ul li a:hover {
  color: #eeeeee;
}

.close-btn {
  margin-top: 10px;
  padding: 10px 20px;
  width: 100%;
  color: #fff;
  border-radius: 20px;
  background-image: linear-gradient(80deg, #585858, #1a4fd8);
  background-size: 400% 400%;
  animation: gradientButton 10s ease infinite;
  cursor: pointer;
  font-size: 22px;
  font-family: "Gilroy", "Inter", sans-serif;
  font-weight: 700;
  border: none;
}

@keyframes gradientButton {
  0% {
    background-position: 0% 50%;
  }

  50% {
    background-position: 100% 50%;
  }

  100% {
    background-position: 0% 50%;
  }
}
/* 
.close-btn {
  margin-top: 10px;
  padding: 10px 20px;
  background-color: #ff5757;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-size: 32px;
}

.close-btn:hover {
  background-color: #ff0000;
} */
</style>
