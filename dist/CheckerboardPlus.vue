<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon checkerboard-plus-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M19 17H22V19H19V22H17V19H14V17H17V14H19V17M8 16H12V12H8V16M12 12H16V8H12V12M2 2V22H13.54C13 21.42 12.63 20.74 12.36 20H8V16H4V12H8V8H4V4H8V8H12V4H16V8H20V12.36C20.74 12.63 21.42 13 22 13.54V2H2Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "CheckerboardPlusIcon",
  props: {
    title: {
      type: String,
      default: "Checkerboard Plus icon"
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
