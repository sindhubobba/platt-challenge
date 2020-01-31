<template>
  <div class="utility">
    <img src="../assets/image/super-tool-day.png">
    <p>{{imageTitle}}</p>
  </div>
</template>

<script>
export default {
  name: "UtilityBox",
  props: {
    imgUrl: String,
    imageTitle: String
  }
};
</script>

<style>
.utility {
  background-color: white;
  padding: 10px;
  width: 20%;
  box-shadow: 0 0 10px #888888;
}

.utility p {
  text-align: center;
  font-weight: 900;
}

.utility img {
  width: 100%;
}
</style>


