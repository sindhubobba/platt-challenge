<template>
  <div class="recent">
    <span>Recently Viewed</span>
    <span id="view">View all</span>
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
  padding: 20px;
  position: relative;
  font-weight: bold;
}
#view {
  position: absolute;
  right: 30px;
  color: green;
  cursor: pointer;
}
.items {
  display: flex;
  justify-content: center;
  margin: 20px 0;
}
.items img {
  margin: 10px;
}
</style>


