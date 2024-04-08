<script setup lang="ts">
import Experiences from './Experiences.vue'
import Educations from './Educations.vue'
import { NCollapse, NCollapseItem } from 'naive-ui';
import Sidebar from './Sidebar.vue';
</script>
<template>
    <div id="header">
        <h1>Eddy Eyme-Rossat</h1>
    </div>
    <div id="wrapper">
        <Sidebar></Sidebar>
        <div style="flex: 1; display: flex; flex-direction: column; width: 100%;">
            <n-collapse :default-expanded-names="['1', '2', '3']" style="flex: 1; width: 100%;">
                <n-collapse-item title="Experiences" name="1">
                    <Experiences></Experiences>
                </n-collapse-item>
                <n-collapse-item title="Formation" name="2">
                    <Educations></Educations>
                </n-collapse-item>
            </n-collapse>

        </div>
    </div>
    <div id="footer">
        <span> Made with 🩷 by me.</span>
        <span>Clonez ce CV ici: <a href=""></a> (Fait par Eddy Eyme-Rossat)</span>
    </div>

</template>
<style scoped>
#wrapper {
    display: flex;
    flex-direction: row;
    gap: .4rem;
}

h1 {
    text-align: center;
}

#footer{
    display: flex;
    flex-direction: column;
    margin-top: 1rem;
}
</style>
