<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon home-thermometer-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M12 2L2 12H4V21H20V12H22M12 5L18 11V19H6V11M12 8C11.45 8 11 8.45 11 9V13.27C10.38 13.63 10 14.29 10 15C10 16.11 10.9 17 12 17S14 16.11 14 15C14 14.29 13.62 13.63 13 13.27V9C13 8.45 12.55 8 12 8Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "HomeThermometerOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Home Thermometer Outline icon"
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
