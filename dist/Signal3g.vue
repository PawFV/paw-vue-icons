<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon signal3g-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M11,16.5V14.25C11,13 10,12 8.75,12C10,12 11,11 11,9.75V7.5A3,3 0 0,0 8,4.5H2V7.5H8V10.5H5V13.5H8V16.5H2V19.5H8A3,3 0 0,0 11,16.5M22,16.5V10.5H17.5V13.5H19V16.5H16V7.5H22V4.5H16A3,3 0 0,0 13,7.5V16.5A3,3 0 0,0 16,19.5H19A3,3 0 0,0 22,16.5Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "Signal3gIcon",
  props: {
    title: {
      type: String,
      default: "Signal3g icon"
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
