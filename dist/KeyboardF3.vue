<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon keyboard-f3-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M5 7H11V9H7V11H10V13H7V17H5V7M19 15C19 16.11 18.11 17 17 17H13V15H17V13H15V11H17V9H13V7H17C18.1 7 19 7.89 19 9V10.5C19 11.33 18.33 12 17.5 12C18.33 12 19 12.67 19 13.5V15Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "KeyboardF3Icon",
  props: {
    title: {
      type: String,
      default: "Keyboard F3 icon"
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
