<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon map-marker-check-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M12,2C15.86,2 19,5.14 19,9C19,14.25 12,22 12,22C12,22 5,14.25 5,9C5,5.14 8.14,2 12,2M10.47,14L17,7.41L15.6,6L10.47,11.18L8.4,9.09L7,10.5L10.47,14Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "MapMarkerCheckIcon",
  props: {
    title: {
      type: String,
      default: "Map Marker Check icon"
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
