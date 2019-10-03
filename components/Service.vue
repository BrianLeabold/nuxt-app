<template>
  <article class="service">
    <nuxt-link :to="'/myservices/'+ id">
      <div class="preview-image" :style="{backgroundImage: 'url('+ thumbnail +')'}">
        <span class="date">{{date}}</span>
      </div>
      <h3>{{title}}</h3>
      <p>{{previewText}}</p>
    </nuxt-link>
  </article>
</template>
<script>
export default {
  props: ['id', 'thumbnail', 'date', 'title', 'previewText']
}
</script>
<style scoped>
a {
  text-decoration: none;
  color: chocolate;
}
.preview-image {
  background-position: center;
  background-size: cover;
  width: 100%;
  height: 200px;
}
.date {
  background: #ccc;
  color: #000;
  padding: 2px 5px;
  bottom: 0;
  left: 0;
}
</style>