<template >
    <header>
        <div class="container">
            <nav>
                <h1>Portfolio.</h1>
                <ul>
                    <li  @click="selectedPage='home'" :class="{active: selectedPage==='home'}">
                        <a href="#">Acceuil</a>
                    </li>
                    <li @click="selectedPage='about'" :class="{active: selectedPage==='about'}">
                        <a href="#about">A Propos</a>
                    </li>
                    <li @click="selectedPage='services'" :class="{active: selectedPage==='services'}">
                        <a href="#services">Services</a>
                    </li>
                    <li @click="selectedPage='portfolio'" :class="{active: selectedPage==='portfolio'}">
                        <a href="#portfolio">Portfolio</a>
                    </li>
                    <li @click="selectedPage='contact'" :class="{active: selectedPage==='contact'}">
                        <a href="#contact">Contact</a>
                    </li>
                    <li>
                        <IconDark></IconDark>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>
<script lang="ts" setup>
import IconDark from './icons/IconDark.vue';
import { ref } from 'vue';
const selectedPage = ref('home')
</script>
<style scoped>
nav{
    display: flex;
    justify-content: space-between;
    padding: 30px 0;
}

ul{
    display: flex;
    gap: 35px;
    align-items: center;
}

h1{
    font-size: 1.5rem;
    font-weight: bold;
    color: var(--vt-c-purple-mute);
}

nav ul li a{
    font-size: 1.2rem;
}

.active{
    border-bottom: 3px solid black;
}
</style>