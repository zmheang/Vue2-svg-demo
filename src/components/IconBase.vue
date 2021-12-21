<template>
  <svg
  xmlns="https://www.w3.org/2000/svg"
  :width="width"
  :height="height"
  viewBox="0 0 18 18"
  :aria-labellebdy="iconName"
  role="presentation">
    <title :id="iconName" lang="en">{{iconName}} icon</title>
    <g :fill="iconColor">
      <slot />
    </g>
  </svg>
</template>

<script>
export default {
  name: "IconBase",
  props: {
    iconName: {type: String, default: 'box'},
    width: {type: [String, Number], default: 18},
    height: {type: [String, Number], default: 18},
    iconColor: {type: String, default: 'currentColor'}
  }
}
</script>

<style scoped>
svg{
  display: inline-block;
  vertical-align: baseline;
  margin-bottom: -2px;
}

</style>