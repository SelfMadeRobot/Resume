<script setup lang="ts">
import SkillComponent from './Skill.vue';
import { ref } from 'vue';
import { Skill } from '../lib/Skill';


const skills = ref<Skill[]>([
    {
        name: 'HTML/CSS',
        value: 100,
        category: 'language'
    },
    {
        name: 'Typescript',
        value: 100,
        category: 'language'
    },
    {
        name: 'Javascript',
        value: 100,
        category: 'language'
    },
    {
        name: 'C#',
        value: 100,
        category: 'language'
    },
    {
        name: 'Golang',
        value: 70,
        category: 'language'
    },
    {
        name: 'Java',
        value: 70,
        category: 'language'
    },
    {
        name: 'Python',
        value: 50,
        category: 'language'
    },
    {
        name: 'VueJs',
        value: 100,
        category: 'framework'
    },
    {
        name: 'React',
        value: 80,
        category: 'framework'
    },
    {
        name: 'ASP.NET',
        value: 100,
        category: 'framework'
    },
    {
        name: 'DOTNET',
        value: 100,
        category: 'framework'
    },
    {
        name: 'ElectronJS',
        value: 80,
        category: 'framework'
    },
    {
        name: 'MongoDB',
        value: 100,
        category: 'database'
    },
    {
        name: 'MySQL',
        value: 100,
        category: 'database'
    },
    {
        name: 'SQL Server',
        value: 70,
        category: 'database'
    },
    {
        name: 'Pack office',
        value: 60,
    },
    {
        name: 'Docker',
        value: 100,
    },
    {
        name: 'Kubernetes',
        value: 100,
    },
    {
        name: 'Firebase',
        value: 100,
    },
    {
        name: 'GCloud',
        value: 60,
    },
    {
        name: 'AWS',
        value: 80,
    },
    {
        name: 'Azure Devops',
        value: 100,
    },
    {
        name: 'Linux',
        value: 70,
    },
    {
        name: 'Git',
        value: 90,
    },
    {
        name: 'NodeJS',
        value: 90,
    },
    {
        name: 'Microservices',
        value: 90,
    },
    {
        name: 'Scrum',
        value: 70,
    },
])
</script>
<template>
    <div id="skills-wrapper">
        <table>
            <tr><td><h3>Langages</h3></td></tr>
            <SkillComponent v-for="(skill, i) in skills.filter(s => s.category && s.category == 'language')" :key="i" :skill="skill"></SkillComponent>
            <tr><td><h3>Frameworks</h3></td></tr>
            <SkillComponent v-for="(skill, i) in skills.filter(s => s.category && s.category == 'framework')" :key="i" :skill="skill"></SkillComponent>
            <tr><td><h3>BDD</h3></td></tr>
            <SkillComponent v-for="(skill, i) in skills.filter(s => s.category && s.category == 'database')" :key="i" :skill="skill"></SkillComponent>
            <tr><td><h3>Autre</h3></td></tr>
            <SkillComponent v-for="(skill, i) in skills.filter(s => !s.category)" :key="i" :skill="skill"></SkillComponent>
        </table>

    </div>
</template>
<style scoped>
#skills-wrapper {
    display: flex;
    flex-direction: column;
    gap: .4rem;
}

td{
    text-align: left;
}
</style>
