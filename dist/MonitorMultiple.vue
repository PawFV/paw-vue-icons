<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon monitor-multiple-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M22,17V7H6V17H22M22,5A2,2 0 0,1 24,7V17C24,18.11 23.1,19 22,19H16V21H18V23H10V21H12V19H6C4.89,19 4,18.11 4,17V7A2,2 0 0,1 6,5H22M2,3V15H0V3A2,2 0 0,1 2,1H20V3H2Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "MonitorMultipleIcon",
  props: {
    title: {
      type: String,
      default: "Monitor Multiple icon"
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
