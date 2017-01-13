<template>
  <div class="container">
    Home 2
    <p>
      <strong>From api: </strong>
      {{title}}
    </p>

    <br/>
    <br/>
    <br/>
    <br/>
    <test-component />
  </div>
</template>

<script>
import axios from 'axios';
import TestComponent from '../components/Test.vue';

export default {
  components: { TestComponent },
  data() {
    return axios.get('http://jsonplaceholder.typicode.com/photos/4').then(res => res.data);
  }
}
</script>

<style>
.container {
  text-align: center;
  padding-top: 100px;
  font-family: sans-serif;
}
</style>
