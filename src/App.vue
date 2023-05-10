<template>
  <div class="app" >
    <v-app>
      <TitleBar @addTask="addTask"/>
      <v-main>
        <TaskView :tasks="list_tasks"  />
      </v-main>
    </v-app>
  </div>
</template>

<script>
import TitleBar from './components/TitleBar.vue';
import TaskView from './components/TaskView.vue';

export default({
  data:()=>({
    list_tasks: [
      {title: 'кря', select: false},
      {title: 'да', select: true},
      {title: 'бывает', select: false}
    ],
    text: "блабла"
    
  }),
  methods:{
    addTask(e){
      if(e!='') this.list_tasks.push({title:e, select:false})
    },
    
  },
  components:{
    TitleBar,
    TaskView
  }
})
</script>
<style>

</style>
