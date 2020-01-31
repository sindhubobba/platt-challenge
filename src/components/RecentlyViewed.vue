<template>
  <div class="recent">
    <div class="title-group">
      <span>Recently Viewed</span>
      <span id="view">View all</span>
    </div>
    <div class="items">
      <img src="../assets/recent/11.png">
      <img src="../assets/recent/22.png">
      <img src="../assets/recent/22.png">
    </div>
  </div>
</template>

<script>
export default {
  name: "RecentlyViewed"
};
</script>

<style>
.recent {
  background-color: white;
  box-shadow: 0 0 10px #888888;
  font-weight: bold;
}
#view {
  color: green;
  cursor: pointer;
}
.items {
  display: flex;
  justify-content: center;
  flex-wrap: wrap
}
.items img {
  margin: 10px;
}
.title-group{
  display:flex;
  justify-content: space-between;
  margin: 20px 10px;
}
@media screen and (max-width: 480px) {
  .recent{
    margin-top: 20px;
  }
}
</style>


