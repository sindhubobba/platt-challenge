<template>
  <div class="market-group">
    <img :src="require(imgUrl)">
    <p>{{imageTitle}}</p>
  </div>
</template>

<script>
export default {
  name: "Markets",
  props: {
    imgUrl: String,
    imageTitle: String 
  },
  created() {
    console.log("img url", this.imgUrl);
  }
};
</script>

<style>
.market-group {
  background-color: white;
  max-width: 109px;
  box-shadow: 0 3px 5px 1px #888888;
}

.market-group p {
  text-align: center;
  font-weight: 900;
}

.market-group img {
  height: 76px;
}
</style>