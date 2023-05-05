<template>
  <div class="app" >
    <div class="title">
      <v-container fluid>
      <v-app-bar elevation="6" >
        <v-spacer>ToDo</v-spacer>
        <v-btn class="mx-4"
               color="indigo" @click="onClick">
            <v-icon dark>
                mdi-plus
            </v-icon>
        </v-btn>
      </v-app-bar>
      
    <AddTask @back="getTask" v-if="add_new"/>
    <v-list>
      <v-list-item-group
          v-model="selected"
          active-class="pink--text"
          multiple
        >
          <template v-for="item in list_tasks" :key="item.title" >
            <v-list-item >
              <template >
                <v-list-item-content >
                  <v-list-item-title v-text="item.title"></v-list-item-title>
                  </v-list-item-content>
                </template>
              
            </v-list-item>
          </template>
        </v-list-item-group>
      </v-list>
  </v-container>
    </div>
    <div></div>
</div>
</template>

<script>
import AddTask from './components/AddTask.vue'
// import TaskView from './components/TaskView.vue';
export default{
  data:()=>({
    add_new: false,
    list_tasks:[
      {title: 'кря'},
      {title:'ага'},
      {title:'да'}
    ]
  }),
  methods:{
    onClick(){
      this.add_new = !this.add_new
    },
    getTask(e){
      this.add_new = false
      if(e!='') this.list_tasks.push(e)
    }
  },
  components:{
    AddTask,
    // TaskView
  }
}
</script>
<style>

</style>
