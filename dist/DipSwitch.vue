<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon dip-switch-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M3,4H7A1,1 0 0,1 8,5V19A1,1 0 0,1 7,20H3A1,1 0 0,1 2,19V5A1,1 0 0,1 3,4M10,4H14A1,1 0 0,1 15,5V19A1,1 0 0,1 14,20H10A1,1 0 0,1 9,19V5A1,1 0 0,1 10,4M17,4H21A1,1 0 0,1 22,5V19A1,1 0 0,1 21,20H17A1,1 0 0,1 16,19V5A1,1 0 0,1 17,4M4,18H6V13H4V18M11,11H13V6H11V11M18,18H20V13H18V18Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "DipSwitchIcon",
  props: {
    title: {
      type: String,
      default: "Dip Switch icon"
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
