<template>
    <div class="person">
        <h1>{{name}}</h1>
        <h1>{{age}}</h1>
        <button @click="showTel">查看联系方式</button>
        <button @click="modifyName">修改名字</button>
        <button @click="modifyAge">修改年龄 </button>
    </div>
</template>
<script lang="ts">
export default {
    name:'Person',
    data() {
        return {
            name:'zhangsan',
            age:18,
            tel:22222
        }
    },
    methods: {
        showTel(){
            alert(this.tel)
        },
        modifyName(){
            this.name = '张三'
        },
        modifyAge(){
            this.age += 1
        }
    },
}
</script>
<style>
.person{
    background-color: skyblue;
    box-shadow: 0 0 10px;
    border-radius: 10px;
    padding: 20px;
  }
  button{
    margin: 0 10px;
  }
</style>