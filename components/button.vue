<template>
  <a :href="link" class="download-cv" :target="target">{{title}}</a>
</template>

<script>
export default {
props: ["title", "link", "target"]
}
</script>

<style>
.download-cv{
  color: #f0b630;
  border: solid 1px #f0b630;
  font-size: 18px;
  padding: 10px 10px;
}
.download-cv:hover{
  background-color:#f0b630;
  color: white;
  text-decoration: none;
  font-weight:500;
}
</style>