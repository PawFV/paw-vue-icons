<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon calendar-multiple-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M21,17V8H7V17H21M21,3A2,2 0 0,1 23,5V17A2,2 0 0,1 21,19H7C5.89,19 5,18.1 5,17V5A2,2 0 0,1 7,3H8V1H10V3H18V1H20V3H21M3,21H17V23H3C1.89,23 1,22.1 1,21V9H3V21M19,15H15V11H19V15Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "CalendarMultipleIcon",
  props: {
    title: {
      type: String,
      default: "Calendar Multiple icon"
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
