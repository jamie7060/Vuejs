<template>
  <div class="card text-white bg-primary">
    <div class="text-left card-header">{{ contenttitle }}</div>
    <div class="text-left container">{{ contentbody }}</div>
    <div class="text-right container">{{ contentdate }}</div>
    <div class="text-left container">댓글</div>
    <div v-for='(comment, j) in contentcomments' :key="j">
      <div class="text-left container">{{ j+1 }}) {{ comment.body }}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Post',
  props: ['contenttitle', 'contentbody', 'contentdate', 'contentcomments']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
