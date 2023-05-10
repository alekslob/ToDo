<template>
  <div class="app" >
    <div class="title">
      <v-app>
      <TitleBar @add_new="show_add"/>
      
      <AddTask @back="getTask" v-if="add_task"/>
      <TaskView :tasks="list_tasks" />
    </v-app>
    </div>
  </div>
</template>

<script>
import TitleBar from './components/TitleBar.vue';
import AddTask from './components/AddTask.vue';
import TaskView from './components/TaskView.vue';

export default({
  data:()=>({
    add_task: false,
    list_tasks: [
      {title: 'кря', select: false},
      {title: 'да', select: true},
      {title: 'бывает', select: false}
    ],
    text: "блабла"
    
  }),
  methods:{
    show_add(){
      this.add_task = !this.add_task
    },
    getTask(e){
      this.add_task = false
      if(e!='') this.list_tasks.push({title:e, select:false})
    },
    
  },
  components:{
    TitleBar,
    AddTask,
    TaskView
  }
})
</script>
<style>

</style>
