<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon swap-horizontal-variant-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M4,6L8,10V7H16A2,2 0 0,1 18,9A2,2 0 0,1 16,11H8A4,4 0 0,0 4,15A4,4 0 0,0 8,19H16V22L20,18L16,14V17H8A2,2 0 0,1 6,15A2,2 0 0,1 8,13H16A4,4 0 0,0 20,9A4,4 0 0,0 16,5H8V2L4,6Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "SwapHorizontalVariantIcon",
  props: {
    title: {
      type: String,
      default: "Swap Horizontal Variant icon"
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
