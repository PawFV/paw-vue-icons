<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon seat-legroom-reduced-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M19.97,19.2C20.15,20.16 19.42,21 18.5,21H14V18L15,14H9A3,3 0 0,1 6,11V3H12V9H17A2,2 0 0,1 19,11L17,18H18.44C19.17,18 19.83,18.5 19.97,19.2M5,12V3H3V12A5,5 0 0,0 8,17H12V15H8A3,3 0 0,1 5,12Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "SeatLegroomReducedIcon",
  props: {
    title: {
      type: String,
      default: "Seat Legroom Reduced icon"
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
