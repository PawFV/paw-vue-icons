<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon square-root-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M11.76,16.83L14.59,14L11.76,11.17L13.17,9.76L16,12.59L18.83,9.76L20.24,11.17L17.41,14L20.24,16.83L18.83,18.24L16,15.41L13.17,18.24L11.76,16.83M2,11H5V11H5L7.29,16.4L10,6H22V8H11.55L8.68,19H6.22L3.68,13H2V11Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "SquareRootIcon",
  props: {
    title: {
      type: String,
      default: "Square Root icon"
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
