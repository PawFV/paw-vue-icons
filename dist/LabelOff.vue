<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon label-off-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M2,4.27L3.28,3L20,19.72L18.73,21L16.63,18.9C16.43,18.96 16.22,19 16,19H5A2,2 0 0,1 3,17V7C3,6.5 3.17,6.07 3.46,5.73L2,4.27M17.63,5.84L22,12L19,16.2L7.83,5H16C16.67,5 17.27,5.33 17.63,5.84Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "LabelOffIcon",
  props: {
    title: {
      type: String,
      default: "Label Off icon"
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
