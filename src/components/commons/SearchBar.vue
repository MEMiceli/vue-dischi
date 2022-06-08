<template>
  <div class="search">
    <div class="form-outline" @input="$emit('searching', searchtext)">
        <input type="search" id="form1" class="form-control" placeholder="Search Genre" aria-label="Search" v-model="searchtext"/>
    </div>
  </div>
</template>

<script>
export default {
    name:'SearchBar',
    data() {
        return{
            searchtext:'',
        }

    }
}
</script>

<style scoped lang="scss">

</style>