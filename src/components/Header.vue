<script setup>
import { Moon, Logs } from 'lucide-vue-next';
import { ref } from 'vue';
import PopUp from './PopUp.vue'; 

const isOpenMenu = ref(false);
const isOpenTheme = ref(false);

const toggleTheme = () => {
    isOpenTheme.value = !isOpenTheme.value;
};

const toggleMenu = () => {
    isOpenMenu.value = !isOpenMenu.value;
};

const closeMenu = () => {
    isOpenMenu.value = false;
};
</script>

<template>
    <header>
        <div class="theme">
            <button class="btn-theme" :class="{ open: isOpenTheme }" @click="toggleTheme">
                <Moon size={24} class="iconTheme" />
            </button>
        </div>

        <div class="hamburguer">
            <button class="btn-hamburger" :class="{ open: isOpenMenu }" @click="toggleMenu">
                <Logs class="icon" color="#000000" />
            </button>
        </div>
    </header>

    <!-- Passa o estado e o método de fechamento como props -->
    <PopUp v-if="isOpenMenu" @close="closeMenu" />
</template>

<style scoped>
header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 327px;
    margin: 35px auto 0px;
    padding: 0 10px;
}

.btn-theme {
    border: none;
    background-color: #eeeeee;
    width: 42px;
    height: 42px;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 16px;
    transition: background-color 0.3s ease-in-out, color 0.3s ease-in-out;
}

.btn-theme.open {
    background-color: #000000;
    color: #ffffff;
}

.btn-hamburger {
    border: none;
    background-color: #fff;
    transition: transform 0.3s ease-in-out;
}

.btn-hamburger.open .icon {
    transform: rotate(90deg);
}

.iconTheme {
    transition: transform 0.3s ease-in-out;
}

.icon {
    transition: transform 0.3s ease-in-out;
}
</style>
