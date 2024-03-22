<template>
  <div class="person">
    <h1>{{ name }}</h1>
    <h1>{{ age }}</h1>
    <h1>{{ a }}</h1>
    <button @click="showTel">查看联系方式</button>
    <button @click="modifyName">修改名字</button>
    <button @click="modifyAge">修改年龄</button>
  </div>
</template>
<!-- <script lang="ts">
export default {
  name: "Person",
}; 
</script> -->
<script setup lang="ts" name="Person">
import { ref } from 'vue';

let name = "zs"; //此时的name 不是响应式的
let age = 11;
let tel = 111111111;
let a = 22;

function showTel() {
  alert(tel);
}
function modifyName() {
  name = "fish";
}
function modifyAge() {
  age += 1;
}
</script>
<style>
.person {
  background-color: skyblue;
  box-shadow: 0 0 10px;
  border-radius: 10px;
  padding: 20px;
}
button {
  margin: 0 10px;
}
</style>