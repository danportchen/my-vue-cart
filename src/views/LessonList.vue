<template>
  <div class="list">
    <LessonItems v-for="lesson in lessons"  :lesson="lesson" :key="lesson.id"/>
  </div>
</template>

<script>
import { mapState, mapActions } from 'vuex';
import LessonItems from './LessonItems';

  export default {
    components:{
      LessonItems,
    },
    computed: {
      ...mapState([ 'lessons' ]),
    },
    methods: {
      ...mapActions(['fetchLessons']),
    },
    mounted() {
      this.fetchLessons();
    },
  };
</script>

<style scoped>
 .list {
   padding-top: 40px;
   text-align: center;
 }
</style>
