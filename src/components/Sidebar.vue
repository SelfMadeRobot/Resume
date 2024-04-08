<script setup lang="ts">
import Skills from './Skills.vue'
import Socials from './Socials.vue';
</script>
<template>
    <div id="sidebar-wrapper">
        <Socials></Socials>
        <div style="display: flex; flex-direction: column;">
            <h3 style="text-align: start;">A propos de moi</h3>
            <p style="max-width: 200px; text-align: start; text-wrap: wrap;">
                Passionné depuis très jeune par la
                technologie, je me suis naturellement
                dirigé vers le développement. Je suis
                curieux de nature et vif d'esprit, toujours
                en recherche d'innovation. Je m'adapte et
                embrasse à bras ouverts les nouveaux
                challenges. Bien qu'étant pragmatique, je
                reste créatif et ouvert d'esprit.
            </p>




        </div>
        <Skills></Skills>
        <div style="display: flex; flex-direction: column;">
            <h3 style="text-align: start;">Hobbies</h3>
            <ul>
                <li>Développement (un vrai geek) 🖥️</li>
                <li>Guitare 🎶</li>
                <li>Jeux vidéo 🎮</li>
                <li>Futurologie 👀</li>
                <li>Escalade</li>
            </ul>




        </div>
        <div style="display: flex; flex-direction: column;">
            <h3 style="text-align: start;">Langues parlées</h3>
            <ul>
                <li>Français (natale)</li>
                <li>Anglais (courant + technique)</li>

            </ul>




        </div>
    </div>

</template>
<style scoped>
#sidebar-wrapper {
    display: flex;
    flex-direction: column;
    gap: .4rem;
    border-radius: 8px;
    background-color: #EEEEEE;
    padding: 1rem;
}

li {
    text-align: start;
}
</style>
