<template>
  <div class="platt-plus">
    <div>
      <img src="@/assets/image/platt-plus.png">
    </div>
    <div>
      <h1>Get started today</h1>
      <h2>
        Become a
        <span id="plus">Platt Plus</span> Member
      </h2>
      <button type="button" name="Learn More">Learn More</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "PlattPlus"
};
</script>

<style>
.platt-plus {
  display: flex;
  flex-wrap: wrap;
  margin: 20px 10px 20px 10px;
  background-color: white;
  height: 100%;
  padding: 30px;
  box-shadow: 0 0 10px #888888;
  align-items: center;
  justify-content: space-around;
}
.platt-plus img {
  margin: auto;
  height: auto;
}
.platt-plus div {
  text-align: center;
}
#plus {
  color: green;
}
button {
  width: 100%;
  height: 50px;
  background-color: #f2f2f2;
  border-radius: 25px;
  font-size: 20px;
  margin-top: 20px;
  text-align: center;
  cursor: pointer;
  border: none;
  color: #737373;
}
h1 {
  margin: 0;
}
h2 {
  margin: 0;
}
</style>


