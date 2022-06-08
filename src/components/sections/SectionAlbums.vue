<template>
    <section>
        <div class="container">
            <div class="row ">
                <SearchBar @searching="filtergenre"/>
                <AlbumItem class="col-12 col-sm-6 col-lg-2 mt-5" v-for="album in albums" :key="album.index" :album="album"/>
                <div class="col-2">2</div>
                <div class="col-2">3</div>
                <div class="col-2">4</div>
                <div class="col-2">5</div>
            </div> 
        </div>
    </section>
</template>

<script>
import axios from 'axios';
import AlbumItem from '../commons/AlbumItem.vue';
import SearchBar from '../commons/SearchBar.vue';
export default {
    name:'SectionAlbums',
    data(){
        return{
            albums:[],
            albumsearched:[],
        }
    },
    components:{
        AlbumItem,
        SearchBar,

    },
    created() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((response) => {
        // handle success
        this.albums = response.data.response;
        })
        .catch((error) => {
        // handle error
        console.log(error);
        });
    },
    methods: {
        filtergenre(searchtext) {
            this.albumsearched = this.albums.filter((album)=> album.genre.toLowerCase().include(searchtext.toLowerCase()));

        }
    }
}
</script>

<style scoped lang="scss">
    // .container{
    //     color: white;
    // }
   

</style>