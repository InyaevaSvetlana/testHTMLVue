<template>
<div class="folder">
  <p class="folder-name">{{name}}</p>
  </div>
  <template v-for="folder in folders">
    <FolderView :name="folder.name" :folders="folder.folders" :files="folder.files"/>
  </template>
  <template v-for="file in files">
    <FileView :name="file.name"/>
  </template>
</template>

<script>
import FileView from "./FileView";
export default {
  name: 'FolderView',
  components: {FileView},
  props: {
    name: String,
    folders:Array,
    files:Array
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.folder{
  color: rgb(255, 255, 255);
  background-image: url(../../img/folder.png);
  background-size: cover;
  height: 80px;
  width: 90px;
  position: relative;
  flex-wrap: wrap;
  font-size: 15px;
  margin: 0 30px;
  cursor: pointer;
}
.folder-name{
  position: absolute;
  top: 50%;
    left: 50%;
    margin-right: -50%;
    transform: translate(-50%, -50%)
}
</style>
