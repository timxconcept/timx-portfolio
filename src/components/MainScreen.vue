<template>
  <div>
    <div class="grid-container">
      <div>
        <h4 class="LeftFade">Brand <br />Designer</h4>
      </div>
      <div><img src="../assets/images/TimxLogo.png" alt="" class="logo" /></div>
      <div>
        <h4 class="RightFade">Motion<br />Designer</h4>
      </div>
      <div>
        <Toggle :mode="mode" @toggle="$emit('toggle')" />
      </div>
      <div>
        <img class="timx_image" src="../assets/images/timx_2.png" alt="" />
      </div>
      <div>
        <p>empty</p>
      </div>
      <div>
        <h4 class="LeftFade">Frontend<br />Designer</h4>
      </div>
      <div class="middle_bottom">
        <p>
          I am an independent hands-on UX/UI-designer helping clients to
          structure and visually brand their (digital) content. While focussing
          on the users’ needs, I craft meaningful aesthetic graphic solutions. I
          aim for innovation, inclusivity and simplicity.
        </p>
        <a
          href="https://www.behance.net/timothyexodus"
          class="social_icons"
          target="_blank"
        >
          <icon name="behance" size="30px" />
        </a>
        <a
          href="https://www.instagram.com/timxdesign/"
          class="social_icons"
          target="_blank"
        >
          <icon name="instagram" size="30px" />
        </a>
        <a href="github.com/timxconcept/" class="social_icons" target="_blank">
          <icon name="github" size="30px" />
        </a>
      </div>
      <div>
        <h4 class="RightFade">UI/UX<br />Designer</h4>
      </div>
    </div>
  </div>
</template>

<script>
import Toggle from "./Toggle.vue";
export default {
  props: ["mode"],
  components: { Toggle },
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
  font-size: 0.6em;
}

div {
  align-items: center;
  margin: 0 auto;
}

h4 {
  text-align: left;
  margin: 0 20px;
  font-size: clamp(0.9em, 2vw, 2em);
}

p {
  text-align: center;
  font-size: clamp(0.6em, 0.9vw, 1em);
  width: clamp(31em, 34vw, 45em);
  margin-bottom: 25px;
}

.logo {
  width: clamp(10em, 15vw, 20em);
}

.timx_image {
  width: clamp(25em, 45vw, 35em);
  animation: fadein 1s;
}

.middle_bottom {
  text-align: center;
}
.social_icons {
  display: inline;
  margin: 10px;
  color: white;
  text-align: center;
}

svg {
  width: clamp(1.5em, 2vw, 4em) !important;
}

.social_icons:hover {
  color: gray;
}

@keyframes fadein {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.LeftFade {
  animation: fadeleft 1s;
}

.RightFade {
  animation: faderight 1s;
}

@keyframes fadeleft {
  from {
    opacity: 0;
    transform: translateX(-50px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes faderight {
  from {
    opacity: 0;
    transform: translateX(50px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}
</style>