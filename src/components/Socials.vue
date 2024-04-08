<script setup lang="ts">
import SocialComponent from './Social.vue'
import { Social } from '../lib/Social'
import { NAvatar } from 'naive-ui';
import { ref } from 'vue';

const socials = ref<Social[]>([
    {
        title: 'Email',
        a: 'eddy.eymepro@gmail.com',
        link: ''
    },
    {
        title: 'LinkedIn',
        a: 'eddy-eyme-rossat-7b7001123',
        link: 'https://www.linkedin.com/in/eddy-eyme-rossat-7b7001123/'
    },
    {
        title: 'Phone',
        a: '06 99 39 11 87',
        link: ''
    }
])
</script>
<template>
    <div>
        <n-avatar round :size="128" src="/profile.png" />
        <SocialComponent v-for="(soc, id) in socials" :key="id" :soc="soc"></SocialComponent>
    </div>
</template>
<style scoped></style>
