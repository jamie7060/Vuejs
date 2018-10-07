<template>
  <div class="border container">
    <div class="textLeft container text">{{ contenttitle }}</div>
    <div class="textLeft container">{{ contentbody }}</div>
    <div class="textRight container">{{ contentdate }}</div>
    <div class="textLeft container">댓글</div>
    <div v-for='(comment, j) in contentcomments' :key="j">
      <div class="textLeft container">{{ j+1 }}) {{ contentcomments.body }}</div>
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
