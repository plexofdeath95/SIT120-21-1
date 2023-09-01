<script setup>
  import { ref } from 'vue';

  const showTitle = true;
  const alternativeTitle = false;
  const showSubtitle = true;
  const items = ['Apple', 'Banana', 'Orange'];
  const inputValue = ref('');
</script>

<template>
 <div id="app">
    <!-- Conditional Rendering using v-if, v-else-if, v-else -->
    <h1 v-if="showTitle">This is the title</h1>
    <h1 v-else-if="alternativeTitle">This is an alternative title</h1>
    <h1 v-else>No Title</h1>

    <!-- Conditional Rendering using v-show -->
    <h2 v-show="showSubtitle">This is the subtitle</h2>

    <!-- Rendering Lists using v-for -->
    <ul>
        <li v-for="item in items">{{ item }}</li>
    </ul>

    <!-- Using v-if with v-for -->
    <ul v-for="item in items">
        <li v-if="item !== 'Banana'">
           <div>{{ item }}</div> 
        </li>
    </ul>

    <!-- Form Input Handlings using v-model -->
    <input type="text" v-model="inputValue">
    <p>Input Value: {{ inputValue }}</p>
</div>
</template>

<style scoped>
h1 {
  color: blue;
}

h2 {
  color: green;
}

ul {
  list-style: none;
}

ul li {
  background-color: lightgray;
  margin: 5px;
  padding: 10px;
}

input {
  border: 2px solid black;
}
</style>
