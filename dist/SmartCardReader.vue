<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon smart-card-reader-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M21 4A2.07 2.07 0 0 0 19 2H5A2.07 2.07 0 0 0 3 4V18H21M8.25 16H7V6H8.25C9.91 6 10.75 9.34 10.75 11S9.91 16 8.25 16M14.5 13.5A2.5 2.5 0 1 1 17 11A2.5 2.5 0 0 1 14.5 13.5M23 21V22H1V21A2 2 0 0 1 3 19H21A2 2 0 0 1 23 21Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "SmartCardReaderIcon",
  props: {
    title: {
      type: String,
      default: "Smart Card Reader icon"
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
