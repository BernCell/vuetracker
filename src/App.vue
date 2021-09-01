<template>
<<<<<<< HEAD
<el-container>

  <el-aside width="200px">
    <TheMenu/>
  </el-aside>

  <el-container>
    <el-header height="60px" >
      
      <TheTopTask />
       
    </el-header>

    <el-main>
      <el-table :data="tableData">
        <el-table-column prop="date" label="Date" width="140">
        </el-table-column>
        <el-table-column prop="name" label="Name" width="120">
        </el-table-column>
        <el-table-column prop="address" label="Address">
        </el-table-column>
      </el-table>
    </el-main>
  </el-container>
</el-container>
</template>




<script>
import TheMenu from "./components/TheMenu.vue"
import TheTopTask from "./components/TheTopTask.vue"
  export default {
    components: { 
      TheMenu, 
      TheTopTask },
    data() {
      const item = {
        date: '2016-05-02',
        name: 'Tom',
        address: 'No. 189, Grove St, Los Angeles'
      };
      return {
        tableData: Array(20).fill(item)
=======
  <el-container class="mainContainer">

    <el-aside width="200px">
      <TheMenu />
    </el-aside>

    <el-container>
      
      <el-header height="60px">
        <TheTopTask />
      </el-header>

      <el-main>
        <TaskList :tasks="tasks" />
      </el-main>

    </el-container>

  </el-container>
</template>

<script>
  import TheMenu from './components/TheMenu.vue'
  import TheTopTask from './components/TheTopTask.vue'
  import TaskList from './components/TaskList.vue'

  export default {
    components: {
      TheMenu,
      TheTopTask,
      TaskList
    },
    data() {
      const sample = {
        name: 'Développement de la feature "edit" d\'un tweet',
        startTime: '01/03/2021',
        endTime: '00:43:13',
      };
      return {
        tasks: Array(20).fill(sample)
>>>>>>> a9d26aa0242399ce81f396fb9c147be2468cd14d
      }
    }
  };
</script>

<style lang="scss">
<<<<<<< HEAD
/* Bonne pratique: utiliser de préférence le style global dans l'App.vue (éventuellement le 'style scoped') 
mais de préférence le 'style scoped' en component.vue  */

body {margin:0}

#app {
=======
body { margin: 0; }
#app {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
>>>>>>> a9d26aa0242399ce81f396fb9c147be2468cd14d
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
<<<<<<< HEAD
  
}

.el-aside {
    color: #333; 
    /* color:var(--el-text-color-primary); */
    /* border-right: solid 1px var(--el-menu-border-color) */
     border-right: solid 1px #e6e6e6;
   } 
    
 .el-header {
   padding: 0 !important;
   border-bottom: solid 1px #e6e6e6;
  /*  background-color: #B3C0D1;
     color: var(--el-text-color-primary); */
    color: #333; 
    line-height: 60px;
    .el-input .el-input__inner{
      border:none !important ;
    }
  }

   
</style>





=======
}
.mainContainer { height: 100%; }

.el-aside {
  height: 100%;
  color: #333;
  border-right: solid 1px #e6e6e6;
}
.el-header {
  padding: 0 !important;
  border-bottom: solid 1px #e6e6e6;
  color: #333;
  line-height: 60px;
  .el-input .el-input__inner {
    border: none !important;
  }
}

</style>
>>>>>>> a9d26aa0242399ce81f396fb9c147be2468cd14d
