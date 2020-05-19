<template>
  <div>
    <li>
      <img class="post-img" :src="commentpost.authorImg" />
      <slot name='beforeName'></slot>
      <small>{{ commentpost.author }}</small>
      <p class="post-comment">"{{ commentpost.text }}"</p>
      <slot name='underComment'></slot>
    </li>
  </div>
</template>

<script>
export default {
  props: ['commentpost']
}
</script>
