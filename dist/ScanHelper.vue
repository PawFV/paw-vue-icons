<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon scan-helper-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M0 2A2 2 0 0 1 2 0H6V2H2V6H0V2M24 22A2 2 0 0 1 22 24H18V22H22V18H24V22M2 24A2 2 0 0 1 0 22V18H2V22H6V24H2M22 0A2 2 0 0 1 24 2V6H22V2H18V0H22Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "ScanHelperIcon",
  props: {
    title: {
      type: String,
      default: "Scan Helper icon"
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
