<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon camera-party-mode-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M12,17C10.37,17 8.94,16.21 8,15H12A3,3 0 0,0 15,12C15,11.65 14.93,11.31 14.82,11H16.9C16.96,11.32 17,11.66 17,12A5,5 0 0,1 12,17M12,7C13.63,7 15.06,7.79 16,9H12A3,3 0 0,0 9,12C9,12.35 9.07,12.68 9.18,13H7.1C7.03,12.68 7,12.34 7,12A5,5 0 0,1 12,7M20,4H16.83L15,2H9L7.17,4H4A2,2 0 0,0 2,6V18A2,2 0 0,0 4,20H20A2,2 0 0,0 22,18V6C22,4.89 21.1,4 20,4Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "CameraPartyModeIcon",
  props: {
    title: {
      type: String,
      default: "Camera Party Mode icon"
    },
    decorative: {
      type: Boolean,
      default: false
    },
    fillColor: {
      type: String,
      default: "currentColor"
    },
    size: {
      type: Number,
      default: 24
    }
  }
}
</script>
