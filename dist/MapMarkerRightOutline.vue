<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon map-marker-right-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M9 6.5C10.38 6.5 11.5 7.62 11.5 9S10.38 11.5 9 11.5 6.5 10.38 6.5 9 7.62 6.5 9 6.5M9 2C12.87 2 16 5.13 16 9C16 14.25 9 22 9 22S2 14.25 2 9C2 5.13 5.13 2 9 2M9 4C6.24 4 4 6.24 4 9C4 10 4 12 9 18.71C14 12 14 10 14 9C14 6.24 11.76 4 9 4M18 17L23 12L18 7V17Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "MapMarkerRightOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Map Marker Right Outline icon"
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
