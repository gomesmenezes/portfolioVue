<script setup lang="ts">
import { Github, Linkedin, Mail } from 'lucide-vue-next';
</script>

<template>
    <div class="social-icons">
        <ul>
            <li>
                <a target="_blank" href="https://github.com/gomesmenezes">
                    <Github color="#171515"/>
                </a>
            </li>
            <li>
                <a target="_blank" href="https://www.linkedin.com/in/jos%C3%A9-gomes-de-menezes/">
                    <Linkedin color="#0e76a8"/>
                </a>
            </li>
            <li>
                <a target="_blank" href="mailto:gomesxdev@gmail.com">
                    <Mail color="#000"/>
                </a>
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