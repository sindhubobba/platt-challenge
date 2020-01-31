<template>
  <div class="pmkt">
    <h3 class="title">Product Markets</h3>
    <div class="markets">
      <div class="market-group">
        <img src="@/assets/image/datacomm.png">
        <p>DataComm</p>
      </div>
      <div class="market-group">
        <img src="@/assets/image/hvac.png">
        <p>HVAC</p>
      </div>
      <div class="market-group">
        <img src="@/assets/image/industrial.png">
        <p>Industrial</p>
      </div>
      <div class="market-group">
        <img src="@/assets/image/lighting.png">
        <p>Lighting</p>
      </div>
      <div class="market-group">
        <img src="@/assets/image/energy.png">
        <p>Energy Efficiency</p>
      </div>
      <div class="market-group">
        <img src="@/assets/image/utility.png">
        <p>Utility</p>
      </div>      
    </div>
  </div>
</template>

<script>
export default {
  name: "ProductMarkets"
};
</script>

<style>
.pmkt {
  padding-right: 10px;
  padding-left: 10px;
}
.pmkt .title {
  font-size: 30px;
  font-weight: 900;
  letter-spacing: 2px;
  text-align: center;
  color: black;
}
.markets {
  display: flex;
  flex-direction: row;
  justify-content: center;
}
.markets > div {
  margin: 0px 10px;
}
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

@media screen and (max-width: 480px) {
  .pmkt {
    display: none;
  }
}
</style>


