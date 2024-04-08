<script setup lang="ts">
import { Social } from '../lib/Social'

defineProps<{ soc: Social }>()
</script>
<template>
    <div id="social-wrapper">
        <h5>{{ soc.title }}</h5>
        <a :href="soc.link">{{ soc.a }}</a>
    </div>
</template>
<style scoped>
#social-wrapper{
    display: flex;
    flex-direction: column;
    gap: .1rem;
}
h5{
    text-align: start;
    padding: 0;
    margin: 0;
}

a{
    text-align: start;
}
</style>
