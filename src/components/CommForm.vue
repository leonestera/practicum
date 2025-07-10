<script>
export default {
    name: 'CommForm',
   data(){
    return {
        newComment: ''
    };
   },
   methods: {
    submitComment() {
         const comment = this.newComment.trim();
      if (comment !== '') {
        this.$emit('addComment', comment); 
        this.newComment = ''; 
      }
    }
   }

}
</script>

<template>
  <div>
    <input v-model="newComment" placeholder="Напишіть коментар..." />
    <button @click="submitComment">Залишити коментар</button>
  </div>
 
</template>

<style scoped>

</style>