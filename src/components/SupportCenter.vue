<template>
  <div class="support-center">
    <div class="support">
      <p class="title">Support Center</p>
      <p class="title phone">800-257-Platt</p>
      <sub>800-257-5288</sub>
      <p class="time">4 a.m. - 12 a.m. (pst)</p>
      <sub class="time">7 Days a week</sub>
      <button>
        <img src="../assets/ic/black/ic_comment.png">
        <span>Live Help</span>
      </button>
    </div>
    <div class="contact">
      <p>Contact Us</p>
      <p>What's New</p>
      <p>FAQ's</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "SupportCenter"
};
</script>

<style>
.support-center {
  background-color: gray;
  text-align: center;
  padding: 20px;
  display: flex;
  flex-direction: column;
}
.title {
  font-size: 30px;
  color: white;
  font-weight: 900;
}
.phone {
  margin: 0;
}
sub {
  font-size: 20px;
  color: white;
  font-weight: bold;
}
.time {
  font-size: 30px;
  color: lightgrey;
  font-weight: 900;
  margin: 20px 0 0 0;
}
.support {
  max-width: 350px;
  margin: auto;
}
.support-center span {
  margin: 20px;
}
.contact {
  color: white;
  margin: 20px 0;
  display: flex;
  justify-content: space-around;
  font-weight: 900;
  font-size: 20px;
}
</style>


