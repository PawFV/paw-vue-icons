<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon lighthouse-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M8,10V8H9V4H8V3L12,1L16,3V4H15V8H16V10H14.74L8.44,13.64L9,10H8M13,8V4H11V8H13M7,23L7.04,22.76L16.15,17.5L16.67,20.88L13,23H7M8.05,16.17L15.31,12L15.83,15.37L7.43,20.22L8.05,16.17Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "LighthouseIcon",
  props: {
    title: {
      type: String,
      default: "Lighthouse icon"
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
