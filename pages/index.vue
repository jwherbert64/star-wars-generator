<template>
  <div class="app">
    <br>
    <br>
    <br>
    <planet
      v-if="planetData[0]"
      :data="planetData[0]"/>
    <planet
      v-if="planetData[1]"
      :data="planetData[1]"/>
    <planet
      v-if="planetData[2]"
      :data="planetData[2]"/>
    <planet
      v-if="planetData[3]"
      :data="planetData[3]"/>
    <br>
    <br>
    <br>
    <character
      v-if="characterData[0]"
      :data="characterData[0]"/>
    <character
      v-if="characterData[1]"
      :data="characterData[1]"/>
    <character
      v-if="characterData[2]"
      :data="characterData[2]"/>
    <character
      v-if="characterData[3]"
      :data="characterData[3]"/>
  </div>
</template>

<script>
  import Planet from '~/components/Planet.vue'
  import Character from '~/components/Character.vue'
  import axios from 'axios'

  export default {
    components: {
      Planet,
      Character,
    },
    data() {
      return {
        planetData: [],
        characterData: [],
      }
    },
    mounted() {
      axios.get('https://swapi.co/api/planets/1/')
        .then((response) => {
          this.planetData.push(response.data);
        }).catch((error) => {
          console.log(error)
        })

      axios.get('https://swapi.co/api/people/1/')
        .then((response) => {
          this.characterData.push(response.data);
        }).catch((error) => {
          console.log(error)
        })

      axios.get('https://swapi.co/api/planets/2/')
        .then((response) => {
          this.planetData.push(response.data);
        }).catch((error) => {
          console.log(error)
        })

      axios.get('https://swapi.co/api/people/5/')
        .then((response) => {
          this.characterData.push(response.data);
        }).catch((error) => {
          console.log(error)
        })

      axios.get('https://swapi.co/api/planets/4/')
        .then((response) => {
          this.planetData.push(response.data);
        }).catch((error) => {
          console.log(error)
        })

      axios.get('https://swapi.co/api/people/14/')
        .then((response) => {
          this.characterData.push(response.data);
        }).catch((error) => {
          console.log(error)
        })

      axios.get('https://swapi.co/api/planets/7/')
        .then((response) => {
          this.planetData.push(response.data);
        }).catch((error) => {
          console.log(error)
        })

      axios.get('https://swapi.co/api/people/25/')
        .then((response) => {
          this.characterData.push(response.data);
        }).catch((error) => {
          console.log(error)
        })

      console.log(this.planetData)
      console.log(this.characterData)
    }
  }
</script>

<style>
  body {
    background-color: #999;
  }

  .app {
    width: 100%;
    height: 100%;
    margin: 0 auto;
    text-align: center;
    font-family: "Lucida Sans Unicode", "Lucida Grande", sans-serif;
    display: inline-block;
  }
</style>
