<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon home-lightbulb-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M12 2L2 12H4V21H20V12H22M12 5L18 11V19H6V11M13.5 14.58V16H10.5V14.58C9.07 13.75 8.57 11.92 9.4 10.5C10.23 9.05 12.07 8.56 13.5 9.38S15.43 12.05 14.6 13.5C14.34 13.94 13.96 14.32 13.5 14.58M13 17H11V18H13V17Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "HomeLightbulbOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Home Lightbulb Outline icon"
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
