<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon engine-off-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M3.78,2.5L21.5,20.22L20.23,21.5L18,19.27V20H10L8,18H5V15H3V18H1V10H3V13H5V10L6.87,8.14L2.5,3.77L3.78,2.5M20,9V12H18V8H12V6H15V4H7.82L22.82,19H23V9H20Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "EngineOffIcon",
  props: {
    title: {
      type: String,
      default: "Engine Off icon"
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
