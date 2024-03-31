<template>
    <a to="#" class="back-to-top" @click="scrollToTop">
        <svg xmlns="http://www.w3.org/2000/svg" width="1.5em" height="1.5em" viewBox="0 0 24 24">
            <path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="M12 6v13m0-13l4 4m-4-4l-4 4" />
        </svg>
    </a>
</template>
<script setup>
import { onMounted, onBeforeUnmount } from 'vue';

const scrollToTop = () => {
    window.scrollTo({
        top: 0,
        behavior: 'smooth'
    });
};

const handleScroll = () => {
    const backToTopButton = document.querySelector('.back-to-top');
    if (backToTopButton) {
        if (window.scrollY > 300) {
            backToTopButton.style.opacity = '1';
            backToTopButton.style.visibility = 'visible';
        } else {
            backToTopButton.style.opacity = '0';
            backToTopButton.style.visibility = 'hidden';
        }
    }
};

onMounted(() => {
    window.addEventListener('scroll', handleScroll);
});

onBeforeUnmount(() => {
    window.removeEventListener('scroll', handleScroll);
});

</script>
<style>
.back-to-top {
    background-color: var(--color-btn-border);
    position: fixed;
    bottom: 20px;
    right: 20px;
    color: var(--color-background);
    padding: 10px;
    border-radius: 3px;
    cursor: pointer;
}
</style>