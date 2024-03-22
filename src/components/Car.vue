<template>
    <div>
        <h2>一辆{{car.brand}}车，价格{{car.price}}万</h2>
        <button @click="changePrice">修改价格</button>
    </div>
    <br>
    <ul>
        <li v-for="g in games" :key="g.id">{{g.name}}</li>
    </ul> 
</template>
<script lang="ts" setup name='car'>
import {reactive} from 'vue'
let car=reactive({brand:"benz",price:100})

let games = [
    {id:1,name:"yuanshen"},
    {id:2,name:"yuanshen2"},
    {id:3,name:"yuanshen3"}
]
function changePrice(){
    car.price += 200
}
</script>
<style>
    
</style>