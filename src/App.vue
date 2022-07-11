<template>
 <div>
   <div class="col-6 mx-auto">
     <add-task @onAddtask="addTask"></add-task>
     <task-list :tasks="tasks"></task-list>
   </div>
 </div>
</template>

<script>
import AddTask from './components/AddTask.vue'
import TaskList from './components/TaskList.vue'

export default {
  name: 'App',
  data() {
    return {
        tasks: [],
        newTask: {name: '',done: false}
    }
  },
  components: {
    AddTask,
    TaskList
  },
  methods: {
   addTask(name){
     this.tasks.push({name: name, done: false})
   }
  }
}
</script>
