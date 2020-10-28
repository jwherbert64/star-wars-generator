<template>
  <div class="frame">
    <div class="name">
      {{ data.name }}
    </div>

    <div :class="`character character--${data.gender}`">
      <div :class="`hair hair--${data.hair_color}`">
      </div>

      <div :class="`skin skin--${data.skin_color}`">
        <div class="eyes">
          <div :class="`eye eye--${data.eye_color}`">
          </div>

          <div :class="`eye eye--${data.eye_color}`">
          </div>
        </div>

        <div class="nos noselol lol">
        </div>

        <div class="mouth">
        </div>
      </div>
    </div>
  </div>
</template>

<script>

  export default {
    props: {
      data: Object,
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

  .character {
    width: 100px;
    height: 100px;
    overflow: hidden;
    display: inline-block;
  }

  .character--male {
    border-radius: 0 0 20px 20px;
  }

  .character--female {
    border-radius: 0 0 30px 30px;
  }

  .hair {
    height: 28px;
  }

  .hair--blond {
    background-color: #FF0;
  }

  .hair--brown {
    background-color: #D2691E;
  }

  .hair--black {
    background-color: #000;
  }

  .skin {
    height: 72px;
  }

  .skin--light {
    background-color: #FDF5E2;
  }

  .skin--fair {
    background-color: #FFE0BD;
  }

  .skin--dark {
    background-color: #9C7248;
  }

  .eyes {
    height: 28px;
    display: flex;
    justify-content: space-around;
  }

  .eye {
    width: 16px;
    height: 16px;
    margin: auto;
    border-radius: 50%;
    display: inline-block;
  }

  .eye--blue {
    background-color: #0163A1;
  }

  .eye--brown {
    background-color: #38101C;
  }

  .nose {
    width: 0;
    height: 0;
    margin: auto;
    border-left: 8px solid transparent;
    border-right: 8px solid transparent;
    border-bottom: 12px solid #D9B082;
  }

  .mouth {
    width: 40px;
    height: 12px;
    margin: auto;
    margin-top: 8px;
    border-bottom-left-radius: 100px;
    border-bottom-right-radius: 100px;
    background: #FFF;
  }
</style>