<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon seal-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M20.39,19.37L16.38,18L15,22L11.92,16L9,22L7.62,18L3.61,19.37L6.53,13.37C5.57,12.17 5,10.65 5,9A7,7 0 0,1 12,2A7,7 0 0,1 19,9C19,10.65 18.43,12.17 17.47,13.37L20.39,19.37M7,9L9.69,10.34L9.5,13.34L12,11.68L14.5,13.33L14.33,10.34L17,9L14.32,7.65L14.5,4.67L12,6.31L9.5,4.65L9.67,7.66L7,9Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "SealIcon",
  props: {
    title: {
      type: String,
      default: "Seal icon"
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
