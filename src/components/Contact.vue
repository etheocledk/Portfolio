<template>
    <div class="container">
        <div>
            <p class="title">Voulez-vous me contacter ? </p>
            <div class="contact__line">
                <img src="../assets/images/blue_highlight_01.svg" alt="">
            </div>
            <p class="contact__text">Vous pouvez utiliser le formulaire de prise de rendez-vous
                ou me laisser directement <br> un message whatsapp sur mon numéro téléphonique.
            </p>
        </div>

        <div class=" contact__content">
            <div>
                <div class="contact__form">
                    <div class="label__container">
                        <label for="name">Votre nom complet :</label>
                        <label for="tel">Numéro téléphonique :</label>
                        <label for="email">Votre adresse e-mail :</label>
                        <label for="message">Votre message :</label>
                    </div>
                    <div class="input__container">
                        <input type="text" placeholder="Votre nom & prénom">
                        <input type="tel" placeholder="Votre numéro téléphonique">
                        <input type="email" placeholder="Votre adresse e-mail">
                        <textarea name="message" id="message" cols="30" rows="10" maxlength="500"
                            placeholder="Votre message..."></textarea>
                        <div class="btn">
                            <input type="submit" value="Envoyer">
                        </div>
                    </div>
                </div>
            </div>
            <div>
                <div class="information__container">
                    <div>
                        <IconLocation></IconLocation>
                    </div>
                    <div class="fa_sharp_sous">
                        <h2>Adresse</h2>
                        <p>Cotonou, BENIN</p>
                        <hr>
                    </div>
                </div>
                <div class="information__container">
                    <div>
                        <IconPhone></IconPhone>
                    </div>
                    <div class="fa_sharp_sous">
                        <h2>Téléphone</h2>
                        <p>+229 56105720</p>
                        <hr>
                    </div>
                </div>
                <div class="information__container">
                    <div>
                        <IconMessage></IconMessage>
                    </div>
                    <div class="fa_sharp_sous">
                        <h2>Adresse e-mail</h2>
                        <p>etheocledk@gmail.com</p>
                        <hr>
                    </div>
                </div>
                <div class="information__container">
                    <div>
                        <IconLink></IconLink>
                    </div>
                    <div>
                        <h2>Réseaux sociaux</h2>
                        <div class="icon__container">
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
                        <hr>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script lang="ts" setup>
import IconFacebook from './icons/IconFacebook.vue';
import IconGithub from './icons/IconGithub.vue';
import IconInstagramVue from './icons/IconInstagram.vue';
import IconLink from './icons/IconLink.vue';
import IconLinkedinVue from './icons/IconLinkedin.vue';
import IconX from './icons/IconX.vue';
import IconMessage from './icons/IconMessage.vue';
import IconPhone from './icons/IconPhone.vue';
import IconLocation from './icons/IconLocation.vue';

</script>
<style scoped>
.title {
    font-size: 4rem;
    font-family: Caveat-Bold;
    color: var(--color-black);
    text-align: center;
    margin-bottom: 5px;
}

.contact__line {
    position: absolute;
    top: 70px;
    right: 460px;
}

.contact__text {
    text-align: center;
    font-size: 1.2rem;
    margin-bottom: 40px;
}

.contact__content {
    display: flex;
    gap: 100px;
    flex-wrap: wrap;
}

.information__container {
    display: flex;
    gap: 10px;
    margin-bottom: 10px;
}

.contact__form {
    display: flex;
    gap: 20px;
}

.btn input {
    color: #FFFFFF;
    background-color: var(--color-btn-border);
    padding: 6px 20px;
    border-radius: 5px;
    font-weight: 600;
    cursor: pointer;
    border: 5px solid;

}

.btn input:hover {
    background-color: var(--vt-c-purple-mute);
}

.btn input:focus {
    border-color: #e9bfde;
}

.label__container {
    display: flex;
    flex-direction: column;
    gap: 35px;
}

.input__container {
    display: flex;
    flex-direction: column;
    gap: 20px;
    width: 450px;
}

.input__container input,
textarea {
    border: 1px solid rgb(207, 207, 207);
    margin-left: 5px;
    width: 100%;
    border-radius: 5px;
    resize: none;
    outline: none;
    padding-left: 10px;
    padding-top: 2px;
}

.input__container input {
    height: 40px;
}

hr {
    width: 220px;
}

.icon__container {
    display: flex;
    gap: 6px;
    align-items: center;
}

@media(max-width: 660px) {
    .label__container {
        display: none;
    }

    .contact__content {
        justify-content: center;
        padding: 0 10px;
    }

    .input__container {
        width: 380px;
    }
}


@media(max-width: 400px) {
    .title {
        font-size: 3rem;
        line-height: 1;
    }

    .input__container {
        max-width: 280px;
    }
}
</style>