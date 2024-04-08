<script setup lang="ts">
import { Skill } from '../lib/Skill'
import { NProgress } from 'naive-ui'
defineProps<{ skill: Skill }>()
</script>
<template>
    <tr id="skill-wrapper">
        <td>{{ skill.name }}</td>
        <td><n-progress type="line" :percentage="skill.value" :indicator-placement="'inside'" processing /></td>
    </tr>
</template>
<style scoped>
td{
    text-align: start;
}
</style>
