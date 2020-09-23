<template>
  <div>
      <input type="text" v-model="textSearch"/>
     <button @click="searchData()">Search</button>
     {{movielist}}
     <hr>
   <!-- <div>
  <b-card
    title="Card Title"
    img-src="https://picsum.photos/600/300/?image=25"
    img-alt="Image"
    img-top
    tag="article"
    style="max-width: 20rem;"
    class="mb-2"
  >
    <b-card-text>
      Some quick example text to build on the card title and make up the bulk of the card's content.
    </b-card-text>
     
    <b-button href="#" variant="primary">Go somewhere</b-button>
  </b-card> -->
<!-- </div> -->
<div>
  <b-embed
    type="iframe"
    aspect="16by9"
    src="https://www.youtube.com/embed/wBcBzJ_oofs"
    allowfullscreen
  ></b-embed>
</div>
  </div>
</template>

<script>
import axios from "axios"
export default {
    data(){
        return{
          movielist:null,
          texeSearch:'',
        }
    },
     mounted:{
        searchData(){
        axios
      .get('https://movie-database-imdb-alternative.p.rapidapi.com'+this.texeSearch+'&limit=100')
      .then(response => {
        this.movielist = response.data.results
      })
      .catch(error => {
        console.log(error)
      })
       
    }
     } 
}
</script>
  
<style>

</style>