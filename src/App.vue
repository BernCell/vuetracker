<template>
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
      }
    }
  };
</script>

<style lang="scss">
/* Bonne pratique: utiliser de préférence le style global dans l'App.vue (éventuellement le 'style scoped') 
mais de préférence le 'style scoped' en component.vue  */

body {margin:0}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  
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





