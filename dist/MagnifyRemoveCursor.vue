<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon magnify-remove-cursor-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M1 1V8L8 1H1M18 16H17.42L16.61 15.19C17.5 14 18 12.5 18 11C18 7.13 14.87 4 11 4C9.5 4 8 4.5 6.79 5.4C3.7 7.72 3.07 12.11 5.39 15.2C7.71 18.29 12.1 18.92 15.19 16.6L16 17.41V18L21 23L23 21L18 16M14.6 13.16L13.18 14.58L11.06 12.45L8.94 14.58L7.5 13.16L9.65 11.04L7.5 8.92L8.94 7.5L11.06 9.63L13.18 7.5L14.6 8.92L12.47 11.04L14.6 13.16Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "MagnifyRemoveCursorIcon",
  props: {
    title: {
      type: String,
      default: "Magnify Remove Cursor icon"
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
