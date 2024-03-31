<template>
    <header>
        <div class="container">
            <nav>
                <h1>Portfolio.</h1>
                <ul>
                    <li @click="selectedPage = 'home'" :class="{ active: selectedPage === 'home' }">
                        <a href="#home" @click="navigateToSection('home')">Accueil</a>
                    </li>
                    <li @click="selectedPage = 'about'" :class="{ active: selectedPage === 'about' }">
                        <a href="#about" @click="navigateToSection('about')">À Propos</a>
                    </li>
                    <li @click="selectedPage = 'services'" :class="{ active: selectedPage === 'services' }">
                        <a href="#services" @click="navigateToSection('services')">Services</a>
                    </li>
                    <li @click="selectedPage = 'portfolio'" :class="{ active: selectedPage === 'portfolio' }">
                        <a href="#portfolio" @click="navigateToSection('portfolio')">Portfolio</a>
                    </li>
                    <li @click="selectedPage = 'contact'" :class="{ active: selectedPage === 'contact' }">
                        <a href="#contact" @click="navigateToSection('contact')">Contact</a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script setup>
import { ref } from 'vue';
const selectedPage = ref('home')

// Define the scrollToSection function
function scrollToSection(sectionId) {
    const section = document.getElementById(sectionId);
    if (section) {
        section.scrollIntoView({ behavior: 'smooth' });
    }
}

// Use the scrollToSection function to navigate
function navigateToSection(sectionId) {
    scrollToSection(sectionId);
    resetScrollBehavior();
}

// Reset scroll behavior after a delay
function resetScrollBehavior() {
    document.body.style.scrollBehavior = 'auto';
    setTimeout(() => {
        document.body.style.scrollBehavior = 'smooth';
    }, 1000);
}
</script>

<style scoped>
nav {
    display: flex;
    justify-content: space-between;
    padding: 30px 0;
}

ul {
    display: flex;
    gap: 35px;
    align-items: center;
}

h1 {
    font-size: 1.5rem;
    font-weight: bold;
    color: var(--vt-c-purple-mute);
}

nav ul li a {
    font-size: 1.2rem;
}

.active {
    border-bottom: 3px solid black;
}
</style>
