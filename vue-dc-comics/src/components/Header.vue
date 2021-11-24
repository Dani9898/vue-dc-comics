<template>
    <header>
      <!-- <img src="..assets/img/dc-logo.png" alt=""> -->
      <div class="header-img"></div>
      <nav>
        <ul>
          <li :class= "voceMenu.active ? 'active' : '' " v-for="voceMenu, i in vociMenuHeader" :key="i">{{voceMenu.text}}</li>
        </ul>
      </nav>
    </header>
</template>

<script>
export default {
  name: 'Header',
  data(){
    return {
      vociMenuHeader: [
        {
          text: "CHARACTERS",
          active: false
        },
        {
          text: "COMICS",
          active: true
        },
        {
          text: "MOVIES",
          active: false
        },
        {
          text: "TV",
          active: false
        },
        {
          text: "GAMES",
          active: false
        },
        {
          text: "COLLECTIBLES",
          active: false
        },
        {
          text: "VIDEOS",
          active: false
        },
         {
          text: "FANS",
          active: false
        },
         {
          text: "NEWS",
          active: false
        },
         {
          text: "SHOP",
          active: false
        }
      ]

    }
  }
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  header {
    background-color: #fff;
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: 10px 0;
      li {
        display: inline-block;
        margin: 0 15px;
          &.active {
            text-decoration: underline;
            color: #0282f9;
          }
      }
  }

  .header-img {
    background: red;
    width: 100px;
    height: 100px;
  }
</style>
