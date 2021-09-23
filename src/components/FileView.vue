<template>
<div class="file">
  <p class="file-name">{{name}}</p>
  </div>
</template>

<script>
export default {
  name: 'FileView',
  props: {
    name: String
  }
}
</script>

<style scoped lang="scss">
.file{
  border: 3px solid;
  border-image-slice: 1;
  margin: 10px 10px 10px 50px;
  width: fit-content;
  padding: 0 5px;
  border-image-source: linear-gradient(to left, #743ad5, #d53a9d);
  background-color: rgb(238, 207, 236);
 
}
.file-name{
  margin: 10px;
}
</style>
