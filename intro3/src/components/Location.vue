<template>
  <div class="location-contain">
    <div class="locations">
       <div class="place">
        <img :src="location.img" width="235" height="300"/>
        <h2>{{ location.name | capitalize }}</h2>
        <p>{{location.desc}}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['location']
}
</script>
