<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon format-wrap-square-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M12,7L17,17H7L12,7M3,3H21V5H3V3M3,7H6V9H3V7M21,7V9H18V7H21M3,11H6V13H3V11M21,11V13H18V11H21M3,15H6V17H3V15M21,15V17H18V15H21M3,19H21V21H3V19Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "FormatWrapSquareIcon",
  props: {
    title: {
      type: String,
      default: "Format Wrap Square icon"
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
