<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon clock-alert-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M12,2C6.47,2 2,6.5 2,12A10,10 0 0,0 12,22C14.25,22 16.33,21.24 18,20V17.28C16.53,18.94 14.39,20 12,20A8,8 0 0,1 4,12A8,8 0 0,1 12,4C15.36,4 18.23,6.07 19.41,9H21.54C20.27,4.94 16.5,2 12,2M11,7V13L16.25,16.15L17,14.92L12.5,12.25V7H11M20,11V18H22V11H20M20,20V22H22V20H20Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "ClockAlertOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Clock Alert Outline icon"
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
