<template>
 <h1> New Vue</h1>

 <p>Below lives HomePAge</p>
 <HomePage/>
</template>

<script>
import { defineComponent } from 'vue';
import HomePage from "@/components/HomePage.vue";


export default defineComponent({
  name:'App',
  components :{
    HomePage

  }
})
</script>

<script setup>

</script>


