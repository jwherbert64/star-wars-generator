<template>
  <div class="frame">
    <div class="name">
      {{ data.name }}
    </div>

    <div class="planet">
      <div v-for="terrain in terrains" :class="`terrain ${terrain}`">
      </div>

      <div class="overlay">
      </div>
    </div>
  </div>
</template>

<script>

  export default {
    data() {
      return {
        terrains: [],
      }
    },
    props: {
      data: Object,
    },
    mounted() {
      this.terrains = this.data.terrain.split(', ')
    }
  }
</script>

<style>
  .frame {
    width: 200px;
    margin-left: 40px;
    margin-right: 40px;
    display: inline-block;
  }

  .name {
    margin-bottom: 10px;
  }

  .planet {
    height: 200px;
    width: 200px;
    position: relative;
    background-color: #bbb;
    border-radius: 50%;
    overflow: hidden;
    display: inline-block;
  }

  .terrain {
    height: inherit;
    width: inherit;
    position: absolute;
    left: 0;
  }

  .forests {
    background-color: #228B22;
    opacity: 0.8;
  }

  .desert {
    background-color: #C2B280;
    opacity: 0.8;
  }

  .grasslands {
    background-color: #6FE300;
    opacity: 0.8;
  }

  .tundra {
    background-color: #D7FFFE;
    opacity: 0.8;
  }

  .mountains {
    background-image: url(https://cdn.clipart.email/0f4e1b81132dff16d3417510c4b0f38a_computer-icons-mountain-clip-art-mountain-png-download-540540-_540-540.png);
    background-size: 24px 24px;
    background-repeat: repeat;
    opacity: 0.5;
  }

  .lakes {
    background-image: url(https://www.seekpng.com/png/full/150-1507062_lake-png-transparent-image-lake-clipart-transparent-background.png);
    background-size: 80%;
    background-repeat: repeat-y;
    opacity: 0.5;
  }

  .overlay {
    height: inherit;
    width: inherit;
    position: absolute;
    left: 0;
    background: radial-gradient(circle, rgba(0, 0, 0, 0) 40%, rgba(50, 50, 50, 0.3) 60%, rgba(50, 50, 50, 1) 70%);
  }
</style>