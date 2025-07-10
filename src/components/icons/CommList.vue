<script>
export default {
    name: 'CommList',
    props: {
        comments: {
            type: Array,
            required: true,
        }
    }
}


</script>

<template>
    <ul>
        <li v-for="(comment, index) in comments" :key="index">{{ comment }}</li>
    </ul>
  
</template>

<style scoped>

</style>