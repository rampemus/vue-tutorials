<template>
  <div class="hello">
    <h1>Message:</h1>
    <h2>Type here: {{ message }}</h2>
    <textarea v-model="message" class='message' id='messagetextarea' rows='8' cols='40'></textarea><br>
  </div>
</template>

<script>
export default {
  name: 'Message',
  data () {
    return {
      message: 'Good message'
    }
  }
}
</script>
