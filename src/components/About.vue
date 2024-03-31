<template>
    <div class="container">
        <div class="about__container">
            <h1>A Propos</h1>
            <!-- <div class="about__content"> -->
            <div class="about__content__left">
                <div class="description">
                    <p> En tant que passionné du développement web et mobile ainsi qu’un designer expérimenté, j’ai
                        eu à
                        concevoir des sites web, des applications mobiles de qualité et des designs attractifs et
                        ergonomiques, qui répondent aux besoins et aux attentes de mes clients en utilisant les
                        dernières
                        technologies et les meilleurs pratiques de développement et de conception.
                    </p>
                    <p class="second">
                        Mon souci du détail et mon sens aigu de l’esthétique me permettent de créer des designs
                        uniques,
                        personnalisés pour chaque projet et d’être reconnu en tant que jeune créatif et innovateur
                        de
                        solution. En tant qu’un jeune et un professionnel, je serai content de mettre mon expertise
                        en
                        œuvre
                        pour vous fournir des services de qualité.
                    </p>
                </div>

                <h2>Outils de conception</h2>
                <div class="tools">
                    <p>Adobe Illustrator</p>
                    <p>Adobe Photoshop</p>
                    <p>Canva</p>
                    <p>Figma</p>
                </div>

                <h2>Technologies et Compétences</h2>
                <div class="tools">
                    <p>HTML</p>
                    <p>CSS</p>
                    <p>Bootstrap</p>
                    <p>Tailwind</p>
                    <p>JavaScript</p>
                    <p>Vue.Js</p>
                    <p>Nuxt.JS</p>
                    <p>Php</p>
                    <p>Laravel</p>
                    <p>Git</p>
                    <p>GitHub</p>
                    <p>GitLab</p>
                    <p>MySql</p>
                    <p>MongoDB</p>
                    <p>PostgreSQL</p>
                    <p>Node.JS</p>
                    <p>Express.Js</p>
                    <p>Docker</p>
                </div>
            </div>
            <!-- <div class="picture">
                    <img src="../assets/images/site m.JPG" width="420px" alt="">
                </div> -->
            <!-- </div> -->
        </div>
        <div class="about__arrow">
            <img src="../assets/images/arrow_doodle_4.svg" alt="" width="80px">
        </div>
    </div>
</template>
<script lang="ts" setup>

</script>
<style scoped>
.about__container h1 {
    font-size: 4rem;
    font-family: Caveat-Bold;
    color: var(--color-black);
    text-align: center;
}

.about__content {
    display: flex;
    justify-content: space-between;
}

.description p {
    text-align: justify;
}

.tools {
    display: flex;
    gap: 15px;
    flex-wrap: wrap;
    margin-top: 1rem;
}

.tools p {
    color: var(--color-background);
    font-weight: 600;
    padding: 5px 8px;
    background-color: var(--color-btn-border);
    border-radius: 20px;
}

.about__content__left {
    width: 100%;
}

.about__arrow {
    position: absolute;
    bottom: -120px;
    left: -40px;
    rotate: -40deg;
}

.about__content__left h2 {
    margin-bottom: 10px;
    color: black;
    font-size: 2rem;
    margin-top: 30px;
    font-family: "Caveat-SemiBold";
}

.picture img {
    border-radius: 10px;
    box-shadow: 10px 10px rgba(0, 0, 0, 0.227);
}

@media(max-width: 400px) {
    .about__container h1 {
        font-size: 3rem;
        line-height: 1;
    }

    .second {
        display: none;
    }
}

@media(max-width: 700px) {

    .about__content__left {
        padding: 20px;
    }
}
</style>