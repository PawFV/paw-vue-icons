<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon swap-vertical-variant-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M18,4L14,8H17V16A2,2 0 0,1 15,18A2,2 0 0,1 13,16V8A4,4 0 0,0 9,4A4,4 0 0,0 5,8V16H2L6,20L10,16H7V8A2,2 0 0,1 9,6A2,2 0 0,1 11,8V16A4,4 0 0,0 15,20A4,4 0 0,0 19,16V8H22L18,4Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "SwapVerticalVariantIcon",
  props: {
    title: {
      type: String,
      default: "Swap Vertical Variant icon"
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
