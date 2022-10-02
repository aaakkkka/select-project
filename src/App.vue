<template>
    <div class="container text-center  mt-5 mb-5">
    <h1 class="mt-5 fw-bolder text-success "> Github Project </h1>
     <div class="table-responsive my-5">
      
      <!-- The table component -->
       <Table :fields='fields' :GithubData ="GithubData"></Table>
     </div>
    
</div>
</template>

<script>
// Importing the table component
import Table from './components/Table.vue'

//importing bootstrap 5
import "bootstrap/dist/css/bootstrap.min.css";

export default {
  name: 'App',
  components: {
    Table
  },
  setup(){

    //An array of values for the data
       const GithubData = [
      {ID:"01", Name: "Project 1", Type:"Python", Builder:"Bob", LOC:"1700"},
     {ID:"02", Name: "Project 2", Type:"Python", Builder:"Kevin", LOC:'1900'},
      {ID:"03", Name: "Project 3", Type:"Java", Builder:"Cat", LOC:'2000'},
     {ID:"04", Name: "Project 4", Type:"Java", Builder:"Jack", LOC:'2100'},
      {ID:"05", Name: "Project 5", Type:"Java", Builder:"Tom", LOC:'2200'},  
    ]

    const fields = [
      'ID','Name','Type','Builder','LOC'
    ]

    return{GithubData,fields}
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

