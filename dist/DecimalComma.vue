<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon decimal-comma-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M10 7A3 3 0 0 1 13 10V13A3 3 0 0 1 7 13V10A3 3 0 0 1 10 7M10 9A1 1 0 0 0 9 10V13A1 1 0 0 0 11 13V10A1 1 0 0 0 10 9M17 7A3 3 0 0 1 20 10V13A3 3 0 0 1 14 13V10A3 3 0 0 1 17 7M17 9A1 1 0 0 0 16 10V13A1 1 0 0 0 18 13V10A1 1 0 0 0 17 9M5 14A1 1 0 0 0 4 15L5 18H6V15A1 1 0 0 0 5 14Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "DecimalCommaIcon",
  props: {
    title: {
      type: String,
      default: "Decimal Comma icon"
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
