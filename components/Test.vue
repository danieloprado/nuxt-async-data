<template>
  <div>
    Test Component
    <br />
    <p>
      <strong>From api: </strong>
      {{title}}
    </p>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return axios.get('http://jsonplaceholder.typicode.com/photos/4').then(res => res.data);
  }
}
</script>
