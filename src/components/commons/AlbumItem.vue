<template>
  <div class="card">
      <img :src="album.poster" alt="">
      <h5>{{album.title}}</h5>
      <h6>{{album.author}}</h6>
      <h6>{{album.year}}</h6>
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
  
  img{
    max-width: 100%;
    padding:.800rem
  }
  h6{
    color: silver;
  }
  h5{
    color: whitesmoke;
  }
}
    


</style>