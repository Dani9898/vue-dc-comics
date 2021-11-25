<template>
    <div class="serie">
        
        <div class="serie-img">
            <img :src="details.thumb" :alt="details.series">
        </div>

        <div class="serie-name">
            <span>{{details.series}}</span>
        </div>
    
    </div>
</template>

<script>
export default {
  name: 'SerieCard',
  props: {
      details: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.serie {
    color: #fff;
    margin: 30px 0;
    width: calc(100% / 6);
    padding: 0 20px;
        
        .serie-img {
            width: 100%;
            height: 200px;
            overflow: hidden;

            img {
            width: 100%;
            }
        }

        .serie-name {
            margin-top: 20px;
        }
}

</style>
