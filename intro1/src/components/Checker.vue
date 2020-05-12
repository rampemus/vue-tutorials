<template>
  <div class='checker'>
    <h1>Check these names:</h1>
    <span v-for='option in options' :key='option'>
      <input
        type='checkbox'
        :id='option.value'
        :value='option.value'
        v-model='checkedNames'>
      <label for='option.value'> {{ option.value }}</label>
    </span>
    <br>
    <span>checked names: {{ checkedNames }}</span>
    <br>
    <h2 v-if='checkedNames.length === 4'>That's the beatles!</h2>
    <h2 v-else>Who are the beatles?</h2>
  </div>
</template>

<script>
export default {
  name: 'Checker',
  data () {
    return {
      checkedNames: [],
      options: [
        { value: 'John' },
        { value: 'Paul' },
        { value: 'George' },
        { value: 'Ringo' }
      ]
    }
  }
}
</script>
