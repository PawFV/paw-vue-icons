<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon text-recognition-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M2 4C2 2.9 2.9 2 4 2H8V4H4V8H2V4M22 20C22 21.11 21.11 22 20 22H16V20H20V16H22V20M4 22C2.9 22 2 21.11 2 20V16H4V20H8V22H4M20 2C21.11 2 22 2.9 22 4V8H20V4H16V2H20M9 7V9H11V17H13V9H15V7H9Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "TextRecognitionIcon",
  props: {
    title: {
      type: String,
      default: "Text Recognition icon"
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
