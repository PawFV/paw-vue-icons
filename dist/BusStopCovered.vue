<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon bus-stop-covered-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M20 3H7V2H6A1.78 1.78 0 0 0 4.59 3H2V5H3.73C2 10.58 2 22 2 22H7V5H20M22 8.5A2.5 2.5 0 1 0 19 11V22H20V11A2.5 2.5 0 0 0 22 8.5M15 11.5V16H14V22H12.5V17H11.5V22H10V16H9V11.5A1.5 1.5 0 0 1 10.5 10H13.5A1.5 1.5 0 0 1 15 11.5M12 6.5A1.5 1.5 0 1 0 13.5 8A1.5 1.5 0 0 0 12 6.5Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "BusStopCoveredIcon",
  props: {
    title: {
      type: String,
      default: "Bus Stop Covered icon"
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
