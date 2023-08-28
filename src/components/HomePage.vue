<template>
    <div>
        Some generic message : {{ message }}

        <br>

        <button @click="incrementCounter">Increment</button>
        <br>
        <span>Counter: {{ counter }}</span>

        <br>

        <button @click="decrementCounter">Decrement</button>
        
    </div>

    <div v-if="textHandler" style="margin-top: 20px;">
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Adipisci impedit enim, 
            cupiditate delectus illum ullam, ab consectetur quae, expedita maiores a molestiae. 
            Itaque animi vitae, pariatur praesentium nihil eligendi laboriosam?</p>
    </div>

    <button  @click="showHideElement">
        {{ textHandler? "Hide" : "Show" }}
    
    </button>

    <div style="margin-top: 20px;">
        <div class="list" v-for= "item in collection" :key="item.name">
            <span>Name: {{ item.name }}</span>
            <span>Age: {{ item.age }}</span>
        </div>
    
    </div>

    <div style="margin-top: 20px;">
        <input type="text">
        <p>Input value:</p>
    
    
    </div>





</template>

<script>
import { defineComponent } from "vue";

export default defineComponent( {
    name: 'HomePage',
})

</script>

<script setup>

import { ref , reactive } from "vue";


const message = "Some generic message"
const counter =ref(0);
const textHandler=ref(true)
const collection = reactive([
    {
        name:'Gabriel',
        age :50,

    },

    {
        name:'Tom',
        age :12,
        
    },
    {
        name:'Sam',
        age :23,
        
    }
])


const incrementCounter = ()=>{
    counter.value++;

}

const decrementCounter = ()=>{
    counter.value--;
    
}

const showHideElement = ()=>{
    textHandler.value=!textHandler.value;

}
</script>