<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon redo-variant-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M10.5,7A6.5,6.5 0 0,0 4,13.5A6.5,6.5 0 0,0 10.5,20H14V18H10.5C8,18 6,16 6,13.5C6,11 8,9 10.5,9H16.17L13.09,12.09L14.5,13.5L20,8L14.5,2.5L13.08,3.91L16.17,7H10.5M18,18H16V20H18V18Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "RedoVariantIcon",
  props: {
    title: {
      type: String,
      default: "Redo Variant icon"
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
