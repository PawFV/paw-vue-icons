<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon home-thermometer-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M12 3L2 12H5V20H19V12H22L12 3M12 8A1 1 0 0 1 13 9V14.27A2 2 0 0 1 14 16A2 2 0 0 1 12 18A2 2 0 0 1 10 16A2 2 0 0 1 11 14.27V9A1 1 0 0 1 12 8Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "HomeThermometerIcon",
  props: {
    title: {
      type: String,
      default: "Home Thermometer icon"
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
