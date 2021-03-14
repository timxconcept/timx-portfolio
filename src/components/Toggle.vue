<template>
  <div class="toggle-wrapper">
    <label class="toggle">
      <input
        type="checkbox"
        :checked="mode === 'dark' ? 'checked' : false"
        @change="$emit('toggle')"
      />
      <span class="toggler round"></span>
    </label>
  </div>
</template>

<script>
export default {
  props: ["mode"],
};
</script>

<style lang="scss" scoped>
@import "./global-style/colors.scss";

.toggle {
  position: relative;
  display: inline-block;
  width: 34px;
  height: 60px;
  background: #ff0000;
  border-radius: 50%;
}
input {
  opacity: 0;
  width: 0;
  height: 0;
}

.toggler {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: $black;
  -webkit-animation: 0.4s;
  transition: 0.4s;
}

.toggler:before {
  position: absolute;
  content: "";
  height: 26px;
  width: 26px;
  left: 4px;
  right: 4px;
  background: $white;
  -webkit-animation: 0.4s;
  transition: 0.4s;
  border-radius: 50%;
}

input:checked + .toggler {
  background: gray;
}

input:focus + .toggler {
  box-shadow: 0 0 2px $white;
}

input:checked + .toggler:before {
  -webkit-transform: translateY(26px);
  -ms-transform: translateY(26px);
  transform: translateY(26px);
}

.toggler.round {
  border-radius: 34px;
}

.toggle.round:before {
  border-radius: 50%;
}
</style>