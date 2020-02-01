<template>
  <div class="recent">
    <div class="title-group">
      <span>Recently Viewed</span>
      <span id="view">View all</span>
    </div>
    <div class="items">
      <img src="../assets/recent/11.png" />
      <img src="../assets/recent/22.png" />
      <img src="../assets/recent/22.png" />
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
  justify-content: space-evenly;
}
.items img {
  padding: 5px;
}
<<<<<<< HEAD
=======

>>>>>>> 930fd07... refactor layout
.title-group {
  display: flex;
  justify-content: space-between;
  padding: 10px 20px;
}
@media screen and (max-width: 480px) {
  .recent {
    width: 100%;
<<<<<<< HEAD
    margin-top: 20px;
=======
>>>>>>> 930fd07... refactor layout
  }
}
</style>


