<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon debug-step-over-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M12,14A2,2 0 0,1 14,16A2,2 0 0,1 12,18A2,2 0 0,1 10,16A2,2 0 0,1 12,14M23.46,8.86L21.87,15.75L15,14.16L18.8,11.78C17.39,9.5 14.87,8 12,8C8.05,8 4.77,10.86 4.12,14.63L2.15,14.28C2.96,9.58 7.06,6 12,6C15.58,6 18.73,7.89 20.5,10.72L23.46,8.86Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "DebugStepOverIcon",
  props: {
    title: {
      type: String,
      default: "Debug Step Over icon"
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
