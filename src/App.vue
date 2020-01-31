<template>
  <div id="app">
    <Header></Header>
    <Categories></Categories>
    <div class="small-items">
      <div>
        <div class="img-group">
          <img src="@/assets/ic/green/ic_line_style.png">
        </div>
        <p>Categories</p>
      </div>
      <div>
        <div class="img-group">
          <img src="@/assets/ic/green/ic_search.png">
        </div>
        <p>Search</p>
      </div>
      <div>
        <div class="img-group">
          <img src="@/assets/ic/green/ic_scanner.png">
        </div>
        <p>Scan</p>
      </div>
    </div>
    <ProductMarkets></ProductMarkets>
    <PlattPlus></PlattPlus>
    <div class="recently-viewed">
      <div>
        <img src="@/assets/panel/deal.png" alt="Todays deal">
      </div>
      <RecentlyViewed></RecentlyViewed>
    </div>
    <Utilities></Utilities>
    <div class="app-banner">
      <img src="@/assets/panel/app-get-banner.png" alt="App Banner">
      <h3>Shop better, download the Platt App today</h3>
    </div>
    <SupportCenter></SupportCenter>
  </div>
</template>

<script>
import Header from "@/components/Header";
import Categories from "@/components/Categories";
import ProductMarkets from "@/components/ProductMarkets";
import PlattPlus from "@/components/PlattPlus";
import RecentlyViewed from "@/components/RecentlyViewed";
import Utilities from "@/components/Utilities";
import SupportCenter from "@/components/SupportCenter";

export default {
  name: "App",
  components: {
    Header,
    Categories,
    ProductMarkets,
    PlattPlus,
    RecentlyViewed,
    Utilities,
    SupportCenter
  }
};
</script>

<style>
* {
  box-sizing: border-box;
}
#app {
  font-family: "Avenir", Verdana, Tahoma, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #262626;
}

body {
  background-color: lightgray;
}

.app-banner {
  background-color: white;
  margin: 20px 10px 20px 10px;
  box-shadow: 0 0 10px #888888;
  text-align: center;
  padding-bottom: 10px;
}

.app-banner img {
  width: 100%;
}
.recently-viewed {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  margin: 20px 10px;
}
.recently-viewed img[alt="Todays deal"] {
  width: 100%;
  height: 100%;
}
.small-items {
  display: none;
}

@media screen and (max-width: 480px) {
  .recently-viewed {
    flex-wrap: wrap;
  }
  .small-items {
    display: flex;
    flex-direction: row;
    text-align: center;
    margin: 10px 0;
    justify-content: center;
  }
  .small-items > div {
    margin: 20px;
  }
  .img-group {
    background-color: white;
    height: 75px;
    width: 75px;
    border-radius: 50%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .small-items p {
    font-weight: bold;
  }
}
</style>
