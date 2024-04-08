<script setup lang="ts">
import { onMounted, ref } from 'vue';
import { Education } from '../lib/Education'
const props = defineProps<{ exp: Education }>()

const paragraph = ref()

onMounted(() => {
    paragraph.value.innerHTML = props.exp.description.replace('\n','<br />')
})
</script>
<template>
    <div id="wrapper">
       <h3>{{ exp.name }}</h3>
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
