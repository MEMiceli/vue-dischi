<template>
  <header>
      <div class="image-logo">
          <img src="../../assets/img/spotify-logo.png" alt="">
      </div>
  </header>
</template>

<script>
export default {
    name: 'BaseHeader',
}
</script>


<style scoped lang="scss">
    header{
        background-color: var(--primary-color);
    }
    .image-logo{
        padding: 1.25rem;
        width: 6.25rem;
        img{
            width:100%;
        }
    }

</style>