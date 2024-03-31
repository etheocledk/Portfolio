<template>
    <div class="container">
        <div class="banner__content">
            <p class="title">Salut, je suis Ethéocle Dohoukpèvi</p>
            <div class="yellow_highlight">
                <img src="../assets/images/yellow_highlight_bold_05.svg" alt="">
            </div>
            <p class="content">En tant que passionné du développement web et mobile, je suis un jeune développeur
                dynamique qui souhaite mettre ses compétences au service des particuliers, des startups et des
                entreprises. </p>
            <div class="green_highlight">
                <img src="../assets/images/green_highlight_03.svg" alt="">
            </div>
            <div class="icone_reseau">
                <a href="https://www.facebook.com/etheocledk.5" target="_blank">
                    <IconFacebook></IconFacebook>
                </a>
                <a href="https://www.linkedin.com/in/etheocledk" target="_blank">
                    <IconLinkedinVue></IconLinkedinVue>
                </a>
                <a href="https://github.com/etheocledk" target="_blank">
                    <IconGithub></IconGithub>
                </a>
                <a href="https://twitter.com/etheocle_dk" target="_blank">
                    <IconX></IconX>
                </a>
                <a href="https://instagram.com/etheocledk?igshid=NTc4MTIwNjQ2YQ==" target="_blank">
                    <IconInstagramVue></IconInstagramVue>
                </a>
            </div>
            <div class="btn">
                <div class="btn__left">
                    <a href="">Me contacter</a>
                </div>
                <div class="btn__right">
                    <a href="./assets/img/Simplify and Professional Graphic Designer Resume -1.pdf" target="_blank"
                        rel="noreferrer" class="cv">↓ Mon CV</a>
                </div>
                <div class="arrow__doodle">
                    <img src="../assets/images/arrow_doodle_1.svg" alt="">
                    <p>Télécharger mon cv ici !</p>
                </div>
            </div>
        </div>
    </div>
</template>
<script lang="ts" setup>
import IconFacebook from './icons/IconFacebook.vue';
import IconGithub from './icons/IconGithub.vue';
import IconInstagramVue from './icons/IconInstagram.vue';
import IconLinkedinVue from './icons/IconLinkedin.vue';
import IconX from './icons/IconX.vue';
</script>
<style scoped>
.banner__content {
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    gap: 20px;
    margin-top: 60px;
}

.content {
    text-align: center;
    font-family: "Caveat-Regular";
    font-size: 2rem;
    max-width: 1000px;
}

.title {
    font-size: 3rem;
    font-family: "Caveat-Bold";
}

.btn {
    display: flex;
    align-items: center;
    gap: 25px;
    margin-bottom: 40px;
    flex-wrap: wrap;
    justify-content: center;
}

.btn__left {
    background-color: var(--color-btn-background);
    padding: 10px 45px;
    border-radius: 3px;
}

.btn__left a {
    color: white;
    font-weight: 600;
}

.btn__right {
    background-color: var(--color-background-soft);
    padding: 10px 45px;
    border-radius: 3px;
}

.btn__right a {
    color: var(--color-btn-border);
    font-weight: 600;
}

.icone_reseau {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 20px;
}

.icone_reseau a {
    padding: 5px;
    border: 2px solid var(--color-btn-border);
    border-radius: 100%;
    box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 12px;
}

.arrow__doodle {
    position: absolute;
    top: 20px;
    right: -185px;
}

.arrow__doodle p {
    color: var(--color-btn-border);
    font-family: "Caveat-SemiBold";
    font-size: 1.5rem;
}

.yellow_highlight {
    z-index: -1;
    position: absolute;
    top: 15px;
    right: 420px;
}

.green_highlight {
    z-index: -1;
    position: absolute;
    top: 120px;
    right: 600px;
}

@media(max-width: 400px) {
    .title {
        font-size: 2rem;
        text-align: center;
    }

    .content {
        font-size: 1.5rem
    }

    .icone_reseau {
        gap: 10px;
    }
}

@media(max-width: 600px) {
    .arrow__doodle {
        display: none;
    }
}
</style>