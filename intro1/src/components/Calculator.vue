<template>
  <div class='calculator'>
    <h1>Calculator</h1>
    <div class='row'>
      <span><input class='numberinput' v-model.number='numbers[0]' type='number'></span>
      <span>+</span>
      <span><input class='numberinput' v-model.number='numbers[1]' type='number'></span>
      <span>=</span>
      <span>{{ numbers[0] + numbers[1] }}</span>
    </div>
    <div>
      <p>My favorite kind of taco thing {{ name }}</p>
    </div>
    <select v-model='name' id='nameselection'>
      <option>A Big taco</option>
      <option>B Mid taco</option>
      <option>C Thic taco</option>
      <option>D Nich taco</option>
    </select>
  </div>
</template>

<script>
export default {
  name: 'Calculator',
  data () {
    return {
      numbers: [1, 2],
      name: ''
    }
  }
}
</script>

<style scope>
.numberinput {
  max-width: 30px;
}
</style>
