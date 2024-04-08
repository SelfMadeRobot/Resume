<script setup lang="ts">
import hljs from 'highlight.js';
import typescript from 'highlight.js/lib/languages/typescript'
import { NConfigProvider, GlobalThemeOverrides } from 'naive-ui'

const themeOverrides: GlobalThemeOverrides = {
  Collapse: {
   titleFontSize: "28px"
  }
}
import Resume from './components/Resume.vue'

hljs.registerLanguage('typescript', typescript)


</script>

<template>
  <n-config-provider :hljs="hljs" :theme-overrides="themeOverrides">
    <Resume></Resume>
  </n-config-provider>
</template>

<style></style>
