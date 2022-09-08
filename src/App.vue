<template>
  <div id="app">
    <MainHeader ></MainHeader>
    <MainContent ></MainContent>
  </div>
</template>

<script>
import MainHeader from './components/MainHeader.vue';
import MainContent from './components/MainContent.vue';

export default {
  name: 'App',
  data(){
    return{
      
    }
  },
  components: {
    MainHeader,
    MainContent,
  },
 
}
</script>

<style lang="scss">
  @import './styles/general.scss'
</style>
