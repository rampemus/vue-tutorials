<template>
  <div class='calculator'>
    <h3>Calculator</h3>
    <div class='row'>
      <span><input
        class='numberinput'
        v-model.number='numbers[0]'
        type='number'></span>
      <span>{{ operator }}</span>
      <span><input
        class='numberinput'
        v-model.number='numbers[1]'
        type='number'></span>
      <span>=</span>
      <span>{{
        operator === '+' ? numbers[0] + numbers[1]
        : operator === '-' ? numbers[0] - numbers[1]
        : operator === '*' ? numbers[0] * numbers[1]
        : operator === '/' ? numbers[0] / numbers[1]
        : numbers[0] % numbers[1]
        }}</span>
    </div>
    <div>
      <p>Calculation done by operator: {{ operator }}</p>
    </div>
    <select v-model='operator' id='nameselection'>
      <option>+</option>
      <option>-</option>
      <option>*</option>
      <option>/</option>
      <option>%</option>
    </select>
  </div>
</template>

<script>
export default {
  name: 'Calculator',
  data () {
    return {
      numbers: [1, 2],
      operator: '+'
    }
  }
}
</script>

<style scope>
.numberinput {
  max-width: 30px;
}
</style>
