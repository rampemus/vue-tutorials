<template>
  <div class="numberlist">
    <h1>NumberList</h1>
      <ul v-for="num in 5" :key="num" >
      <li>{{ num }} Some text</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'NumberList'
}
</script>
