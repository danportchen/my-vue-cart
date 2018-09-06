<template>
  <div>
    <Header/>
    <LessonList/>
  </div>
</template>

<script>
  import Header from './views/Header.vue';
  import LessonList from './views/LessonList.vue';
  
  export default {
    components: {
      Header,
      LessonList,
    },
  };
</script>

<style>

</style>
