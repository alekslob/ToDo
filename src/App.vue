<template>
  <div class="app" >
    <div class="title">
      ToDo
    </div>
    <AddTask @click:back="true"/>
    <div></div>
</div>
</template>

<script>
import AddTask from './components/AddTask.vue'
export default{
  components:{
    AddTask
  }
}
</script>
<style>
.app{
  width: 50%;
  margin: 0 auto;
  text-align: center;
}
</style>
