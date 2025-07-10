<script>
import CommForm from './components/CommForm.vue';
import CommList from './components/icons/CommList.vue';

export default {
  name: 'App',
  components:{CommForm,CommList},
  data(){
    return {
      comments: [],
    }
  },
  methods: {
addComment(newComment){
  this.comments.push(newComment);
}
  }
}
</script>

<template>
  <div>
  <h2>Коментарі:</h2>
  <CommList :comments="comments"/>
  <h3>Залишити новий коментар:</h3>
 <CommForm @addComment="addComment"/> 
  </div>
</template>

<style scoped>

</style>
