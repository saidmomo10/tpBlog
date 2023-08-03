<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
// import { createClient } from '@supabase/supabase-js';

// const supabaseUrl = 'https://kesnnwgnwdrvhlxdzlyp.supabase.co';
// const supabaseKey = 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6Imtlc25ud2dud2RydmhseGR6bHlwIiwicm9sZSI6ImFub24iLCJpYXQiOjE2OTEwODQzMDcsImV4cCI6MjAwNjY2MDMwN30.lpBbpoE7mSns62O7vL_-ex2xLyCGqn6B39VH28K61BM';
// const supabase = createClient(supabaseUrl, supabaseKey);
import NavBar from '../components/NavBar.vue'
import { ref } from "vue";
import img3 from "@/assets/img3.jpeg";
import DetailsVue from "./Details.vue";

const articles = ref([
  {
    img: img3,
    title: "Comment devenir riche ?",
    summary: "lorem ipsum jknjoo ijoio",
    id: "1",
    voir: "voir",
    Content :"Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis esse laudantium similique ullam consectetur adipisci expedita qui rerum enim, a, nesciunt consequatur voluptatum illum sit animi reprehenderit veritatis autem necessitat",
  },

  {
    img: img3,
    title: "Comment devenir riche ?",
    summary: "lorem ipsum jknjoo ijoio",
    id: "2",
    voir: "voir",
    Content :"Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis esse laudantium similique ullam consectetur adipisci expedita qui rerum enim, a, nesciunt consequatur voluptatum illum sit animi reprehenderit veritatis autem necessitat",
  },

  {
    img: img3,
    title: "Comment devenir riche ?",
    summary: "lorem ipsum jknjoo ijoio",
    id: "3",
    voir: "voir",
    Content :"Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis esse laudantium similique ullam consectetur adipisci expedita qui rerum enim, a, nesciunt consequatur voluptatum illum sit animi reprehenderit veritatis autem necessitat",
  },

  {
    img: img3,
    title: "Comment devenir riche ?",
    summary: "lorem ipsum jknjoo ijoio",
    id: "4",
    voir: "voir",
    Content :"Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis esse laudantium similique ullam consectetur adipisci expedita qui rerum enim, a, nesciunt consequatur voluptatum illum sit animi reprehenderit veritatis autem necessitat",
  },

  {
    img: img3,
    title: "Comment devenir riche ?",
    summary: "lorem ipsum jknjoo ijoio",
    id: "5",
    voir: "voir",
    Content :"Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis esse laudantium similique ullam consectetur adipisci expedita qui rerum enim, a, nesciunt consequatur voluptatum illum sit animi reprehenderit veritatis autem necessitat",
  },

  {
    img: img3,
    title: "Comment devenir riche ?",
    summary: "lorem ipsum jknjoo ijoio",
    id: "6",
    voir: "voir",
    Content :"Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis esse laudantium similique ullam consectetur adipisci expedita qui rerum enim, a, nesciunt consequatur voluptatum illum sit animi reprehenderit veritatis autem necessitat",
  },

  {
    img: img3,
    title: "Comment devenir riche ?",
    summary: "lorem ipsum jknjoo ijoio",
    id: "7",
    voir: "voir",
    Content :"Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis esse laudantium similique ullam consectetur adipisci expedita qui rerum enim, a, nesciunt consequatur voluptatum illum sit animi reprehenderit veritatis autem necessitat",
  },
]);
</script>

<template>
    <NavBar/>
    <div class="wrapper">
      <section class="content">
        <div class="container">
          <ul class="gallery">
            <li v-for="element in articles" class="gallery_competence">
              <img :src="element.img" alt="" />
              <h5>{{ element.id }}</h5>
              <h3>{{ element.title }}</h3>
              <p>{{ element.summary }}</p>
              <a href="./Details">{{ element.voir }}</a>
            </li>
          </ul>
          <ul id="categories">
            <li id="cat"></li>
          </ul>
        </div>
      </section>
    </div>


  <RouterView />
</template>

<style scoped>
.container {
  max-width: calc(100% - 100px);
  margin: 0 auto;
}

li img{
    width: 300px;
}

.gallery {
  list-style: none;
  width: 70%;
  margin: 0 auto;
  padding: 0 auto;
  padding-top: 50px;
  display: grid;
  grid-template-columns: repeat(auto-fit, 300px);
  grid-auto-rows: 300px;
  grid-gap: 80px;
  justify-content: center;
}
</style>
