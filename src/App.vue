<template>
    <Person/>
    <Car/>
</template>

<script lang="ts">
import Person  from './components/Person.vue'
import Car from './components/Car.vue'
export default {
  name:"App",
  components:{Person,Car}
}
</script>
<style>
</style>