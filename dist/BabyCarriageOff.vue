<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon baby-carriage-off-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M22 10C22 5.6 18.4 2 14 2V10H22M14.2 11H22C22 12.8 21.4 14.5 20.3 15.9C21 16.5 21.4 17.4 21.5 18.3L14.2 11M20.8 22.7L22.1 21.4L2.4 1.7L1.1 3L9.1 11H7.4L6.5 9H3V11H5.2C5.2 11 7.1 15.1 7.3 15.4C6.3 15.9 5.6 16.9 5.5 18C5.2 19.9 6.6 21.7 8.5 22C10.4 22.3 12.2 20.9 12.5 19H14.6C14.7 19.4 14.8 19.8 15 20.2C15.9 21.9 18.1 22.5 19.7 21.6L20.8 22.7M10.5 18.5C10.5 19.3 9.8 20 9 20S7.5 19.3 7.5 18.5 8.2 17 9 17 10.5 17.7 10.5 18.5M18.1 20C17.2 20 16.5 19.3 16.5 18.5V18.4L18.1 20Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "BabyCarriageOffIcon",
  props: {
    title: {
      type: String,
      default: "Baby Carriage Off icon"
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
