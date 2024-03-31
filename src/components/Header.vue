<template>
    <header>
        <div class="container">
            <nav>
                <h1>Portfolio.</h1>
                <ul class="nav">
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
                <div class="menu_container">
                    <div class="menu" @click="manage">
                        <span class="line"></span>
                        <span class="line2"></span>
                        <span class="line3"></span>
                    </div>
                </div>
            </nav>

            <div class="menu_nav_container">
                <div class="menu_nav">
                    <ul>
                        <li @click="closeNav">
                            <a href="#home" @click="navigateToSection('home')">Accueil</a>
                        </li>
                        <li @click="closeNav">
                            <a href="#about" @click="navigateToSection('about')">À Propos</a>
                        </li>
                        <li @click="closeNav">
                            <a href="#services" @click="navigateToSection('services')">Services</a>
                        </li>
                        <li @click="closeNav">
                            <a href="#portfolio" @click="navigateToSection('portfolio')">Portfolio</a>
                        </li>
                        <li @click="closeNav">
                            <a href="#contact" @click="navigateToSection('contact')">Contact</a>
                        </li>
                    </ul>
                </div>
            </div>
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

const manage = () => {
    const line = document.querySelector('.line');
    if (line.classList.contains('hide')) {
        line.classList.remove('hide');
        document.querySelector('.line2').style.transform = 'rotate(0deg)';
        document.querySelector('.line3').style.transform = 'rotate(0deg)';
        document.querySelector('.menu_nav_container').classList.remove('active')
    } else {
        line.classList.add('hide');
        document.querySelector('.menu_nav_container').classList.add('active')
        document.querySelector('.line2').style.transform = 'rotate(45deg)';
        document.querySelector('.line3').style.transform = 'rotate(-45deg)';
    }
}

const closeNav = () => {
    document.querySelector('.menu_nav_container').classList.remove('active')
    document.querySelector('.line').classList.remove('hide');
    document.querySelector('.line2').style.transform = 'rotate(0deg)';
    document.querySelector('.line3').style.transform = 'rotate(0deg)';
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

.menu {
    position: absolute;
    right: 10px;
    top: 5px;
    /* background-color: red; */
    width: 40px;
    display: flex;
    flex-direction: column;
    gap: 6px;
    justify-content: center;
    align-items: center;
    z-index: 30;
}

.line {
    display: inline-block;
    background-color: black;
    width: 100%;
    height: 4px;
    border-radius: 4px;
}

.line2 {
    display: inline-block;
    background-color: black;
    width: 100%;
    height: 4px;
    border-radius: 4px;
}

.line3 {
    display: inline-block;
    background-color: black;
    width: 100%;
    border-radius: 4px;
    height: 4px;
}

.hide,
.menu_container {
    display: none;
}

.menu_nav_container {
    display: none;
}

.menu_nav {
    position: fixed;
    right: 0;
    top: 0;
    background-color: rgba(255, 255, 255, 0.97);
    height: 100vh;
    width: 350px;
    z-index: 10;
    display: flex;
    justify-content: center;
    align-items: center;
}

.active {
    display: block;
}

.menu_nav ul {
    display: flex;
    flex-direction: column;
    gap: 30px;
}

.menu_nav ul li a {
    font-weight: 600;
    font-size: 20px;
}

@media(max-width: 1050px) {
    .menu_container {
        display: block;
    }

    .nav {
        display: none;
    }
}
</style>
