<template>
  <header>
    <h1>{{title}}</h1> <!-- It came from the props-->
    <Button text="Add" color="green" /> <!-- It's a Componenet not just a button tag-->
    <Button text="Update" color="aqua" />
    <Button text="Delete" color="red" />
  </header>
</template>

<script>
import Button from './Button.vue'
export default {
  name: 'Header',  // This header will be use like tag in html.
  props:{
      title:String,
  },
  components:{
      Button
  }

                               //IMPORTANT Lesson
  /*1. props:['title'] *///this props will be only use like a class and  in css. for example <Header title="Task tracer" />


   // Check the below for the default props in the front-end and delete the title props

  /*2. props:{
       title:{
           type:String,
           default:'hello world(default if there is no props)'
       }
   }*/
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
  
}
</style>