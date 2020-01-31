<template>
  <div class="categories">
    <div class="item1">
      <div class="menu-group">
        <div class="menu-img">
          <img src="@/assets/ic/black/ic_categories.png" alt="search">
        </div>
        <div class="menu-header">Shop all categories</div>
      </div>
    </div>
    <div class="item2">
      <div class="menu-group">
        <div class="menu-img">
          <img src="@/assets/ic/black/ic_playlist_add_check.png" alt="search">
        </div>
        <div class="menu-title">My Catalog</div>
      </div>
    </div>
    <div class="item2">
      <div class="menu-group">
        <div class="menu-img">
          <img src="@/assets/ic/black/ic_list.png" alt="search">
        </div>
        <div class="menu-title">My List</div>
      </div>
    </div>
    <div class="item2">
      <div class="menu-group">
        <div class="menu-img live-help">
          <img id="help" src="@/assets/ic/black/ic_chat.png" alt="search">
        </div>
        <div class="menu-title">Live Help</div>
      </div>
    </div>
    <div class="item2">
      <div class="menu-group">
        <div class="menu-img">
          <img src="@/assets/ic/black/ic_check_circle.png" alt="search">
        </div>
        <div class="menu-title">PIM</div>
      </div>
    </div>
    <div class="item2">
      <div class="menu-group">
        <div class="menu-img">
          <img src="@/assets/ic/black/ic_playlist_add_check.png" alt="search">
        </div>
        <div class="menu-title">Account</div>
      </div>
    </div>
    <div class="item2">
      <div class="menu-group">
        <div class="menu-img">
          <img src="@/assets/ic/black/ic_place.png" alt="search">
        </div>
        <div class="menu-title">Branch Locations</div>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  name: "Categories"
};
</script>

<style>
.categories {
  background-color: darkgray;
  display: grid;
  grid-gap: 1px;
  grid-template-columns: 1fr 1fr 1fr;
  border: 1px solid darkgray;
  text-align: center;
}
.menu-group {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
.menu-group > div {
  margin-right: 20px;
}
.menu-group > div:last-child {
  margin: none;
}
.menu-img {
  height: 14px;
  width: 14px;
}
.menu-header {
  font-size: 20px;
  font-weight: 900;
}
.item1 {
  grid-column: 1 / span 3;
}
.item1,
.item2 {
  padding: 25px;
  background: white;
}
.item1 img,
.item2 img {
  /* width: 14px; */
  height: 14px;
}

@media screen and (max-width: 480px) {
  .categories {
    display: flex;
    flex-direction: column;
    text-align: left;
  }
  .menu-group {
    justify-content: flex-start;
  }
  .categories > div {
    border-bottom: 1px solid gray;
  }
  .menu-header::after, .menu-title::after {
    content: url('../assets/ic/black/ic_arrow_forward.png');
    position: absolute;
    right: 20px;
  }
  .live-help {
    background-image: url("../assets/ic/green/ic_chat_active.png");
    height: 14px;
  }
  #help{
    display:none;
  }
}
</style>