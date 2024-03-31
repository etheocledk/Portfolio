<template>
    <div>
        <div class="wrapper">
            <div class="">
                <Header></Header>
                <main>
                    <div class="main__container">
                        <section id="home">
                            <Home></Home>
                        </section>
                        <section class="about__section" id="about">
                            <About></About>
                        </section>
                        <section id="services">
                            <Service></Service>
                        </section>
                        <section id="portfolio" class="portfolio__section">
                            <Portfolio></Portfolio>
                        </section>
                        <section id="contact">
                            <Contact></Contact>
                        </section>
                    </div>
                </main>
                <Footer></Footer>
                <ReturnToTop></ReturnToTop>
            </div>
        </div>
    </div>
</template>
<script lang="ts" setup>
import Home from '@/components/Home.vue';
import Header from '@/components/Header.vue';
import Footer from '@/components/Footer.vue';
import About from '@/components/About.vue';
import Contact from '@/components/Contact.vue';
import Portfolio from '@/components/Portfolio.vue';
import Service from '@/components/Service.vue';
import ReturnToTop from '@/components/ReturnToTop.vue';
</script>
<style>
.main__container section {
    margin-bottom: 60px;
}

.about__section {
    background-color: var(--color-background-soft);
    padding: 20px 0 50px 0;
    border-top-left-radius: 150px;
    border-bottom-right-radius: 150px;
}

.portfolio__section {
    background-color: var(--color-background-soft);
    padding: 20px 0 50px 0;
}
</style>