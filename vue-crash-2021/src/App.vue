<template>
  <div class="container">
    <!--  using components-->
    <!--  $Header$ came from the  scripts component what have been imported from the src/component/header.vue-->
    <!--  $title$ is a props we made it in the src/component/header.vue file-->
    <Header title="Task Tracer" />
    <Tasks :tasks="tasks1"/>                    <!-- V-bind-->
    <!-- remember to use / while using components-->
  </div>
</template>

<script>
import Header from "./components/Header.vue"
import Tasks from "./components/Tasks.vue"

export default {
  name: "App",
  components: {
    Header,
    Tasks,
  },
  data() {
    return{
      tasks1:[]
    }
  },
  created(){
    this.tasks1=[
      {
      id:1,
      text:'Doctors apointment',
      day:'march 1st 2pm',
      reminder:'true'
    },
    {
      id:2,
      text:'teacher apointment',
      day:'march 1st 2pm',
      reminder:'true'
    },
    {
      id:1,
      text:'embassy apointment',
      day:'march 1st 2pm',
      reminder:'false'
    }
    ]
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap");
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: "Poppins", sans-serif;
}
.container {
  max-width: 500px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 1px solid steelblue;
  padding: 30px;
  border-radius: 5px;
}
.btn {
  display: inline-block;
  background: #000;
  color: #fff;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  border-radius: 5px;
  cursor: pointer;
  text-decoration: none;
  font-size: 15px;
  font-family: inherit;
}
.btn:focus {
  outline: none;
}
.btn:active {
  transform: scale(0.98);
}
.btn-block {
  display: block;
  width: 100%;
}
</style>
