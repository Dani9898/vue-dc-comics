<template>
    <header>
      
      <img src="../assets/img/dc-logo.png" alt="">
      <nav>
        <ul>
          <li :class= "voceMenu.active ? 'active' : '' " v-for="voceMenu, i in vociMenuHeader" :key="i"><a href="#">{{voceMenu.text}}</a></li>
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
        
        &.active a {
          border-bottom: 5px solid #0282f9;
          color: #0282f9
        }

        a {
          text-decoration: none;
          padding-bottom: 48px;
        }
      }
  }
</style>
