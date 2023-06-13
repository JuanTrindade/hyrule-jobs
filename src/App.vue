<template>
  <div class="container">
    <h1>Hello World</h1>
    <p>{{ name }} - {{ age }}</p>
    <button @click="changeName('Zelda')" class="button">change name</button>
    <button @click="changeAge(29)" class="button">Change Age</button>
  </div>
</template>

<script lang="ts">
  import { defineComponent } from 'vue';

  export default defineComponent({
    name: 'App',
    components: {},
    data() {
      return {
        name: 'Link',
        age: 25 as number | string
      }
    },
    methods: {
      changeName(name: string) {
        this.name = name
      },
      changeAge (age: number | string){
        this.age = age
      }
    }
  });
</script>

<style>
  .button {
    background-color: #2ecc71; 
    color: #FFF; 
    font-weight: bold; 
    padding: 8px; 
    border-radius: 3px; 
    cursor: pointer;
    border: none;
    width: 15%;
    margin-top: 2%;
  }
  .container{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
</style>
