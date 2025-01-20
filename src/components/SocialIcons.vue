<script setup lang="ts">
import { Github, Linkedin, Mail } from 'lucide-vue-next';
</script>

<template>
    <div class="social-icons">
        <ul>
            <li>
                <Github />
            </li>
            <li>
                <Linkedin />
            </li>
            <li>
                <Mail />
            </li>
        </ul>
    </div>
</template>

<style scoped>

ul {
    display: flex;
    gap: 25px;
    align-items: center;
    justify-content: center;
    padding: 0;
}

li {
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 42px;
    width: 42px;
    background-color: #eeeeee;
    list-style: none;
    border-radius: 16px;
}

</style>