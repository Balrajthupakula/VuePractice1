<template>
    <div>
      <h1>Data Modification Example</h1>
      <p>Current Number: {{ number }}</p>
      <button @click="updateNumber">Update Number</button>
    </div>
  </template>
  
  <script>
  export default {
    name:'LifeCycle', 
    data() {
      return {
        number: 5,
      };
    },
    created() {
      this.number += 10; // Modification in created hook
      console.log('Created Hook - Modified Number:', this.number);
    },
    mounted() {
      this.number += 20; // Modification in mounted hook
      console.log('Mounted Hook - Modified Number:', this.number);
    },
    methods: {
      updateNumber() {
        this.number += 30; // Update number when button is clicked
      },
    },
  };
  </script>
  