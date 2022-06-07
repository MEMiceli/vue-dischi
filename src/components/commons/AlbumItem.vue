<template>
  <div class="card">
      <img :src="album.poster" alt="">
      <h4>{{album.title}}</h4>
      <h5>{{album.uthor}}</h5>
      <h5>{{album.year}}</h5>
  </div>
</template>

<script>
export default {
  name: 'AlbumItem',
  props:{
    album: Object,
  }

}
</script>

<style scoped lang="scss">
.card{
  background-color: var(--primary-color);
  text-align: center;
  color: white;
  padding:.625rem
  img{
    max-width: 100%;
  }
}
    


</style>