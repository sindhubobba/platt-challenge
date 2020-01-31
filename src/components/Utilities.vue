<template>
  <div class="utilities">
    <div class="utility-group">
      <img src="../assets/image/super-tool-day.png">
      <p>Super Tool Day & Dynamic Data Day</p>
    </div>
    <div class="utility-group">
      <img src="../assets/image/ic_location_b.png">
      <p>Branch Locations</p>
    </div>
    <div class="utility-group">
      <img src="../assets/image/ic_helpcenter.png">
      <p>Help Center</p>
    </div>
    <div class="utility-group">
      <img src="../assets/image/ic_platt-u.png">
      <p>Platt University</p>
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
  justify-content: center;
  padding: 0 10px 0 10px;
}
.utility-group {
  background-color: white;
  padding: 10px;
  box-shadow: 0 3px 5px 1px #888888;
  max-width: 200px;
  width: 200px;
  height: 200px;
  text-align: center;
}

.utilities > div {
  margin: 10px 20px;
}

.utility-group p {
  font-weight: 900;
}

.utility-group img {
  display: block;
  margin-left: auto;
  margin-right: auto;
  margin-top: 20px;
}

@media screen and (max-width: 480px) {
  .utilities {
    flex-wrap: wrap;
  }
}
</style>


