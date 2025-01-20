<script lang="ts">
import Header from './components/Header.vue';
import CardMain from './components/CardMain.vue'
import SocialIcons from './components/SocialIcons.vue';
import Experience from './components/Experience.vue';
import Work from './components/Work.vue';

export default {
    components: {
        Header,
        CardMain,
        SocialIcons,
        Experience,
        Work
    }
}
</script>

<template>
    <Header />
    <CardMain />
    <SocialIcons />
    <Experience />
    <Work />
</template>

<style scoped></style>
