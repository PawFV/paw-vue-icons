<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon keyboard-f12-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M2 7H8V9H4V11H7V13H4V17H2V7M16 7H20C21.11 7 22 7.9 22 9V11C22 12.11 21.11 13 20 13H18V15H22V17H16V13C16 11.9 16.9 11 18 11H20V9H16V7M10 7H14V17H12V9H10V7Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "KeyboardF12Icon",
  props: {
    title: {
      type: String,
      default: "Keyboard F12 icon"
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
