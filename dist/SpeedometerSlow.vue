<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon speedometer-slow-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M12 16C13.66 16 15 14.66 15 13C15 11.88 14.39 10.9 13.5 10.39L3.79 4.77L9.32 14.35C9.82 15.33 10.83 16 12 16M12 3C10.19 3 8.5 3.5 7.03 4.32L9.13 5.53C10 5.19 11 5 12 5C16.42 5 20 8.58 20 13C20 15.21 19.11 17.21 17.66 18.65H17.65C17.26 19.04 17.26 19.67 17.65 20.06C18.04 20.45 18.68 20.45 19.07 20.07C20.88 18.26 22 15.76 22 13C22 7.5 17.5 3 12 3M2 13C2 15.76 3.12 18.26 4.93 20.07C5.32 20.45 5.95 20.45 6.34 20.06C6.73 19.67 6.73 19.04 6.34 18.65C4.89 17.2 4 15.21 4 13C4 12 4.19 11 4.54 10.1L3.33 8C2.5 9.5 2 11.18 2 13Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "SpeedometerSlowIcon",
  props: {
    title: {
      type: String,
      default: "Speedometer Slow icon"
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
