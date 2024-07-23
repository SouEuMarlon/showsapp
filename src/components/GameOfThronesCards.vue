<script setup>
  import axios from 'axios';

  const response = await axios.get('https://thronesapi.com/api/v2/Characters')
  console.log(response.data)
</script>

<template>
  <div>
    <h1>Game of Thrones Cards</h1>
    <h2>{{response.length}}</h2>
  </div>
</template>