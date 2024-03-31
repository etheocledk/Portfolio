<template>
    <footer>
        <div class="footer__container">
            <div class="container">
                <div>
                    © Copyright <span v-text="fullyear"></span>. Made by
                    <a rel="noreferrer" target="_blank" href="#">Ethéocle DOHOUKPEVI</a>
                </div>
            </div>
        </div>
    </footer>
</template>
<script lang="ts" setup>
import { ref } from 'vue';
const fullyear = ref()
const date = new Date()
fullyear.value = date.getFullYear()
</script>
<style scoped>
.footer__container {
    background: var(--color-footer-background);
    color: white;
    padding: 20px 0;
    display: flex;
    justify-content: center;
}
</style>