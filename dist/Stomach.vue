<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon stomach-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M4 18C4.67 19.85 6.07 22 12 22C14.36 22 17.07 21.93 19 20C20 19 22 17 22 11S20 4 18 4C16.62 4 15 4 14 6V6.03A1.82 1.82 0 0 1 12.13 6.95C11 6.81 11 6.37 11 6V2H9V6A2.92 2.92 0 0 0 12 9C13 9 13 10.78 13 12C13 13.89 12.5 15.26 11 16C8.69 17.15 6.39 17 5.61 15.47A1.5 1.5 0 0 0 3.14 14.87A3.67 3.67 0 0 0 2 18V22H4Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "StomachIcon",
  props: {
    title: {
      type: String,
      default: "Stomach icon"
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
