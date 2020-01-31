<template>
  <div id="header">
    <img src="../assets/image/logo.png" alt="logo">
    <div class="images">
      <img src="@/assets/ic/white/ic_search.png" alt="search">
      <img src="@/assets/ic/white/ic_shopping_cart.png" alt="shopping cart">
      <img src="@/assets/ic/white/ic_person.png" alt="account">
      <img src="@/assets/ic/white/ic_menu.png" alt="menu">
    </div>

    <div class="search-bar">
      <input
        type="text"
        v-model="searchText"
        @input="onChange" 
        @keydown="onKeyDown"
        @keydown.enter="onEnter" 
        @keydown.esc="onEscape"      
        placeholder="What are you looking for?"
      >
      <img src="@/assets/ic/black/ic_search.png" style="width:30px;height:30px;" alt="search">
      <div class="auto-suggest-container" v-show="showAutosuggest">        
        <ul class="auto-suggest">
          <li v-if="noMatchFound">
            No matches found
          </li>
          <li v-else
            class="auto-suggest-list"
            v-for="(result,i) in results"
            :key="i"
            :class="[selectedIndex === i ? 'focus' : '']"
            @click="setResult(result)">
            <AutosuggestItem :item="result.name"></AutosuggestItem>
            </li>
        </ul>        
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import AutosuggestItem from "./AutosuggestItem"
export default {
  name: "Header",
  components:{AutosuggestItem},
  data() {
    return {
      searchText: "",
      results: [],
      showAutosuggest: false,
      noMatchFound: false,
      selectedIndex: 0
    };
  },
  methods: {
    async onChange() {      
      if(this.searchText !== ""){        
        await axios.get("https://jsonplaceholder.typicode.com/users").then(response => {        
        this.results = response.data.filter(
          user =>
            user.name.toLowerCase().indexOf(this.searchText.toLowerCase()) > -1
        );
      });
        this.showAutosuggest = true;
        if (this.results.length > 0) {          
          this.noMatchFound = false;
        }
        else{         
          this.noMatchFound = true;
        }
      }      
    },
    setResult(result) {
      this.searchText = result.name;
      this.showAutosuggest = false;
    },
    onKeyDown(e){
      if (!this.searchText.length) {
        return;
      }
      if (e.keyCode === 38 && this.selectedIndex > 0) {
        this.selectedIndex--;
      }
      if (e.keyCode === 40 && this.selectedIndex >= 0 && this.selectedIndex < this.results.length - 1) {        
        this.selectedIndex++;
      }      
    }, 
    onEnter(){      
      this.setResult(this.results[this.selectedIndex]);
      this.selectedIndex = 0;
    }, 
    onEscape(){
      this.showAutosuggest = false;
    }

  },
  watch: {
    searchText(val) {
      if (val === "") {        
        this.showAutosuggest = false;
      }
    }
  }
};
</script>

<style>
#header {
  height: 150px;
  width: 100%;
  background-color: green;
  padding: 20px;
  position: relative;
}
.search-bar {
  position: relative;
  width: 100%;
  margin-top: 20px;
}
.search-bar input {
  width: 100%;
  height: 50px;
  border: 1px hidden black;
  border-radius: 5px;
  box-shadow: 0;
  padding: 0 10px;
  font-size: 15px;
}
.search-bar img {
  position: absolute;
  right: 10px;
  top: 10px;
}
.images {
  display: inline-flex;
  width: 200px;
  flex-direction: row;
  justify-content: space-evenly;
  position: absolute;
  right: 0;
}
.auto-suggest {
  list-style: none;
  background-color: white;
  margin: 0;
  padding: 10px;
}
.auto-suggest-list {
  margin-bottom: 15px;
  cursor: pointer;
}
/* .auto-suggest-list:hover{
  text-decoration: underline;
} */
input:focus {
  outline: none;
}
.auto-suggest-list:hover, .focus {
  font-weight: bold;
}
</style>


