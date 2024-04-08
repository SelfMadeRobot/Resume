<script setup lang="ts">
import { onMounted, ref } from 'vue';
import { Experience } from '../lib/Experience'
const props = defineProps<{ exp: Experience }>()

const paragraph = ref()

onMounted(() => {
    paragraph.value.innerHTML = props.exp.content.replace('\n','<br />')
})
</script>
<template>
    <div id="wrapper">
       <h3>{{ exp.title }}</h3>
       <h4>{{ exp.duration }}</h4>
       <p ref="paragraph"></p>
    </div>
</template>
<style scoped>
#wrapper {
    display: flex;
    flex-direction: column;
    justify-content: start;
    gap: .4rem;
    /* background-color: red; */
    border-radius: 8px;
    padding: .4rem;
}

h3{
    text-align: start;
    padding: 0;
    margin: 0;
}
h4{
    text-align: start;
    padding: 0;
    margin: 0;
}

p{
    text-align: start;
}
</style>
