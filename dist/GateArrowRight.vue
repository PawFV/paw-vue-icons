<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon gate-arrow-right-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M15 5V10H13V6H11V10H9V8H7V20H9V18H11V20H12.09A6 6 0 0 1 12 19A6 6 0 0 1 13 15.69V12H15V13.81A6 6 0 0 1 17 13.09V12H19V13.09A6 6 0 0 1 21 13.81V12H22V10H21V5H19V10H17V5H15M9 12H11V16H9V12M19 16V18H15V20H19V22L22 19L19 16Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "GateArrowRightIcon",
  props: {
    title: {
      type: String,
      default: "Gate Arrow Right icon"
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
