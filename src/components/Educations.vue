<script setup lang="ts">
import { Education } from '../lib/Education';
import { NTimeline, NTimelineItem } from 'naive-ui';
import { ref } from 'vue';
import EducationComponent from './Education.vue';


const experiences = ref<Education[]>([
    {
        name: 'Faculté des sciences de Marseille Saint-Jérôme (Aix-Marseille Université)',
        duration: '2018-2020',
        description: 'Master en Electronique, Energie électrique et Automatique (3EA)',
        location: ''
    },
    {
        name: 'IUT de Salon de Provence (Aix-Marseille Université)',
        duration: '2017-2018',
        description: 'Licence professionnelle Systèmes automatisés et Réseaux industriels (SARI)',
        location: ''
    },
    {
        name: `IUT d'Aix-en-Provence Gaston-Berger (Aix-Marseille Université)`,
        duration: '2015-2017',
        description: 'Master en Electronique, Energie électrique et Automatique (3EA)',
        location: ''
    },
    {
        name: 'Lycée Maurice Janetti Saint-Maximin La Sainte Baume',
        duration: '2012-2015',
        description: `BAC S Option Science de l'Ingénieur (SI)`,
        location: ''
    },
])
</script>
<template>
    <div id="exp-wrapper">
        <n-timeline>
            <n-timeline-item v-for="(exp, i) in experiences" :key="i" type="warning" >
                <EducationComponent :exp="exp"></EducationComponent>
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
