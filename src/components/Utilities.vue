<template>
  <div class="utilities">
    <div class="utility-group">
      <div>
        <img src="../assets/image/super-tool-day.png" />
      </div>
      <p class="utility-title">Super Tool Day & Dynamic Data Day</p>
    </div>
    <div class="utility-group">
      <div>
        <img src="../assets/image/ic_location_b.png" />
      </div>
      <p class="utility-title">Branch Locations</p>
    </div>
    <div class="utility-group">
      <div>
        <img src="../assets/image/ic_helpcenter.png" />
      </div>
      <p class="utility-title">Help Center</p>
    </div>
    <div class="utility-group">
      <div>
        <img src="../assets/image/ic_platt-u.png" />
      </div>
      <p class="utility-title">Platt University</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Utilities"
};
</script>

<style>
.utilities {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
}
.utility-group {
  background-color: white;
  box-shadow: 0 3px 5px 1px #888888;
  padding: 5px 10px;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  width: 160px;
}
<<<<<<< HEAD
=======

>>>>>>> 930fd07... refactor layout
.utility-group p {
  font-weight: 900;
  max-width: 150px;
}
.utility-group img {
  height: 90px;
}
.utility-title {
  text-align: center;
}
@media screen and (max-width: 480px) {
  .utilities {
    flex-wrap: wrap;
  }
  .utility-group {
    width: 150px;
    margin: 5px;
  }
}
</style>


