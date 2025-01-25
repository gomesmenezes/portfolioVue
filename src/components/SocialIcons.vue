<script setup lang="ts">
import { Github, Linkedin, Mail } from 'lucide-vue-next';

const links = {
    link: {
        github: 'https://github.com/gomesmenezes',
        linkedin: 'https://www.linkedin.com/in/jos%C3%A9-gomes-de-menezes/',
        mail: 'mailto:gomesxdev@gmail.com'
    }
}

</script>

<template>
    <div class="social-icons">
        <ul>
            <li>
                <a target="_blank" :href="links.link.github" rel="noopener noreferrer">
                    <Github color="#171515"/>
                </a>
            </li>
            <li>
                <a target="_blank" :href="links.link.linkedin" rel="noopener noreferrer">
                    <Linkedin color="#0e76a8"/>
                </a>
            </li>
            <li>
                <a target="_blank" :href="links.link.mail" rel="noopener noreferrer">
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
    height: 58px;
    width: 58px;
    background-color: #eeeeee;
    list-style: none;
    border-radius: 16px;
}
</style>