<template>
  <div>
    <div class="grid-container">
      <div>
        <h4>Brand Design<br />Consultant</h4>
      </div>
      <div><img src="../assets/images/TimxLogo.png" alt="" /></div>
      <div>
        <h4>Motion<br />Designer</h4>
      </div>
      <div>4</div>
      <div>
        <img class="timx_image" src="../assets/images/timx_2.png" alt="" />
      </div>
      <div>6</div>
      <div>
        <h4>Frontend<br />Designer</h4>
      </div>
      <div>
        <div class="social_icons">
          <icon name="behance" size="30px" />
        </div>
        <div class="social_icons">
          <icon name="instagram" size="30px" />
        </div>
        <div class="social_icons">
          <icon name="github" size="30px" />
        </div>
      </div>
      <div>
        <h4>UI/UX<br />Designer</h4>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MainScreen",
};
</script>

<style lang="scss" scoped>
@import "./global-style/colors.scss";

.grid-container {
  display: grid;
  grid-template-columns: 25vw 50vw 25vw;
  grid-template-rows: 25vh 50vh 25vh;
  grid-gap: 0px;
  background-color: $black;
}

div {
  align-items: center;
  margin: 0 auto;
}

h4 {
  text-align: left;
  margin: 0 20px;
}

.timx_image {
  width: 25vw;
}

.social_icons {
  display: inline;
  margin: 10px;
  color: white;
}
</style>