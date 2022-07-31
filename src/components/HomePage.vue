<script setup lang="ts">
import { ref } from 'vue';
import { languages } from './languages';
import Header from './Header.vue';
import Main from './Main.vue';
import Footer from './Footer.vue';

const language = ref('cz')
const languageReturn = ref(languages.czech)

const changeLanguage = () => {
  language.value = language.value === 'cz' ? 'en' : 'cz'
  languageReturn.value = language.value === 'cz' ? languages.czech : languages.english
}

</script>
<template>
  <Header type="home" @change="changeLanguage" />
  <Main v-bind="languageReturn" />
  <Footer />
</template>
<style scoped lang="scss">
</style>