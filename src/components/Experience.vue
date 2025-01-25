<script setup>
import reactCard from '../assets/img/react.png';
import nodeCard from '../assets/img/node.png';
import prismaCard from '../assets/img/prisma.png';
import vueCard from '../assets/img/vue.png';
import typescriptCard from '../assets/img/typescript.png';
</script>

<template>
    <div class="text-experience">
        <h1>EXPERIENCE WITH</h1>
    </div>

    <div class="cards-skills">
        <div class="first-line">
            <ul>
                <li class="react-card"> 
                    <img :src="reactCard" alt="React">
                </li>
                <li class="node-card">
                    <img :src="nodeCard" alt="Node.js">
                </li>
                <li class="prisma-card">
                    <img :src="prismaCard" alt="Prisma">
                </li>
            </ul>
        </div>

        <div class="second-line">
            <ul>
                <li class="vue-card"> 
                    <img :src="vueCard" alt="Vue.js">
                </li>
                <li class="typescript-card">
                    <img :src="typescriptCard" alt="TypeScript">
                </li>
            </ul>
        </div>
    </div>
</template>

<style scoped>
.text-experience {
    max-width: 327px;
    margin: 50px auto 20px;
}

.text-experience h1 {
    font-family: 'Poppins', 'Inter', sans-serif;
    font-weight: 500;
    font-size: 45px;
    text-align: left;
    color: #111827;
    margin: 0px;
}

.cards-skills .first-line  ul{
    width: 327px;
    margin: 0 auto;
    gap: 25px;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0;
}

.cards-skills .second-line  ul{
    width: 327px;
    margin: 0 auto 60px;
    gap: 25px;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0;
}

.second-line {
    margin-top: 20px;
}

li {
    list-style: none;
}

.react-card, .node-card, .prisma-card, .vue-card, .typescript-card {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 84px;
    height: 84px;
    border-radius: 20px;
}

.react-card {
    background-color: #38BDF8;
}

.node-card {
    background-color: #84CC16;
}

.prisma-card {
    background-color: #00618A;
}

.vue-card {
    background-color: #3D986F;
}

.typescript-card {
    background-color: #F0F2F3;
}

</style>