<!-- the script is where the js code goes -->
<script setup>
import { ref } from "vue" // you need this to use ref()

let name = ref("...")
let Newname = ref("")


function AddName(){

name.value = name.value + Newname.value
console.log (name)

}

</script>



<!-- the template is where the html code goes -->
<template>



<div id="navbar" class="container">  
        <div id="title">Mohammad's bootcamp website</div>
        
        
        
        <div id="logo">
            <img src="./assets/cow.jpg" alt="macad cow">
          
        </div>
        

    </div>

    <div id="flex">

        <div id="sidebar" class="container"> 
          
             
        <input type = ”text” v-model="Newname"  placeholder="Add your name to the list:">
        <button id="saveButton" @click="AddName">Save</button>
        

        </div>

        <div id="main" class="container"> 
           
          <h2>{{ name }}</h2>
        </div>
    </div>

</template>



<!-- style is where the css code goes -->
<style scoped>



body{

    margin:0;
}

div{

    /* put the borders in the inside of container */
    box-sizing: border-box;
}

img{

    height: 100%;
    width: auto;

}

#navbar{

    height: 100px;
    border-color: red;


}

#flex{
    
    display: flex;
    height: calc(100vh - 50px);
}

#sidebar{
    
    width:30%;
    border-color: blue;

}

#main{
    width:70%;
    border-color: green;

}

#title{
    width: 70%;
    float:left;
}

#logo{
    width: 30%;
    height: 100%;
    float:right;
    text-align: right;

}

.container{

    border-style: dotted;
    border-width: 1px;

}

</style>