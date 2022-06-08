<template>
  <main>
      <SectionAlbums/>
  </main>
</template>

<script>
import SectionAlbums from '../sections/SectionAlbums.vue';

export default {
    name: 'BaseMain',
    components:{
        SectionAlbums,
    },

}
</script>

<style scoped lang="scss">
    main{
        background-color: #1E2D3B;
    }


</style>