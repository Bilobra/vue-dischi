<template>
  <div id="app">
    <MainHeader @search="onChange"></MainHeader>
    <MainContent :search="changeGenre"></MainContent>
  </div>
</template>

<script>
import MainHeader from './components/MainHeader.vue';
import MainContent from './components/MainContent.vue';

export default {
  name: 'App',
  data() {
    return {
      changeGenre: '',
    }
  },
  components: {
    MainHeader,
    MainContent,
  },
  methods: {
    onChange(data) {
      this.changeGenre = data;
    }
  },

}
</script>

<style lang="scss">
@import './styles/general.scss';
</style>
