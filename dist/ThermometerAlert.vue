<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon thermometer-alert-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M17 12V7H19V12H17M17 16V14H19V16H17M13 13V5C13 3.34 11.66 2 10 2S7 3.34 7 5V13C4.79 14.66 4.34 17.79 6 20S10.79 22.66 13 21 15.66 16.21 14 14C13.72 13.62 13.38 13.28 13 13M10 4C10.55 4 11 4.45 11 5V8H9V5C9 4.45 9.45 4 10 4Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "ThermometerAlertIcon",
  props: {
    title: {
      type: String,
      default: "Thermometer Alert icon"
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
