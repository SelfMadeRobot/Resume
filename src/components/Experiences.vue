<script setup lang="ts">
import { Experience } from '../lib/Experience';
import { NTimeline, NTimelineItem } from 'naive-ui';
import { ref } from 'vue';
import ExperienceComponent from './Experience.vue';


const experiences = ref<Experience[]>([
    {
        title: 'Developper Full Stack - Freelance',
        duration: `Février 2024 - Aujourd'hui`,
        content: `<ul>
    <li>Développement de modules applicatifs pour le logiciel AppVision</li>
    <li>Conversion d'un client Lourd WPF en client léger React</li>
    <li>Création d'un formulaire web permettant l'enregistrement des visiteurs sur un site sensible</li>
    </ul>
`
    },
    {
        title: 'Project Lead Developper - Prysm-Software - Aix-en-Provence',
        duration: '2021 - Janvier 2024',
        content: `Pilotage du projet de Cloudification et de SaaSification du logiciel hyperviseur de
sûreté/sécurité AppVision:
<ul>
    <li>Organisation et pilotage des réunions de suivi</li>
    <li>Architecure de microservices</li>
    <li>Documentation technique</li>
    <li>C#, ASP .net / dotnet6</li>
    <li>Typescript, Vite + VueJS</li>
    <li>Kubernetes</li>
    <li>AWS</li>
    <li>EKS</li>
    <li>ECS</li>
    <li>RDS</li>
    <li>DocumentDB</li>
    <li>Route53</li>
    <li>Docker</li>
    <li>Docker swarm</li>
    <li>MongoDB</li>
    <li>MySQL</li>
    <li>GoLang</li>
    <li>CI/CD Azure DevOps (Pipelines, Artifacts)</li>
    <li>Scrum</li>
    </ul>
`
    },
    {
        title: 'Ingénieur support et formation - Prysm-Software - Aix-en-Provence',
        duration: '2020-2021',
        content: `<ul>
            <li>Traitement des tickets, support technique sur la configuration avancée du
logiciel d'hypervision AppVision</li>
            <li>Documentation client sur l'utilisation du logiciel</li>
            <li>Formation des clients</li>
            <li>Tests qualité</li>
            </ul>`
    },
    {
        title: '(Alternance) Chef de projet en automatisme - MENSY - Les Pennes Mirabeau',
        duration: '2018-2020',
        content: `Etude et mise en oeuvre - Automatisme industriel - Supervision - Documentation -
Rétro-analyse - Rédaction d'analyses fonctionnelles`
    },
    {
        title: '(Alternance) Technicien en automatisme - MENSY - Les Pennes Mirabeau',
        duration: '2017-2018',
        content: `Programmation d'automates industriels (Schneider, WAGO, Siemens) - Programmation
de supervisions (PCVUE, WINCC, Ignition)`
    },
    {
        title: '(Alternance) Chef de projet en automatisme - MENSY - Les Pennes Mirabeau',
        duration: '2018-2020',
        content: ``
    }
])
</script>
<template>
    <div id="exp-wrapper">
        <n-timeline>
            <n-timeline-item v-for="(exp, i) in experiences" :key="i" type="success" :line-type="i == 0? 'dashed' : 'default'">
                <ExperienceComponent :exp="exp"></ExperienceComponent>
            </n-timeline-item>

        </n-timeline>
    </div>
</template>
<style scoped>
#exp-wrapper {
    display: flex;
    flex-direction: column;
    gap: .4rem;
}

h2 {
    text-align: left;
    border-bottom: 2px solid;
}
</style>
