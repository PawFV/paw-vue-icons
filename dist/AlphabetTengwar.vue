<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon alphabet-tengwar-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M10 7L12.5 3H15L11 7H10M12.5 9C11.96 9 11.46 9.13 11 9.35V9H8V11H9V21H11V12.5C11 11.67 11.67 11 12.5 11C13.33 11 14 11.67 14 12.5V14.5C14 15.33 13.33 16 12.5 16H12V18H12.5C14.43 18 16 16.43 16 14.5V12.5C16 10.57 14.43 9 12.5 9Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "AlphabetTengwarIcon",
  props: {
    title: {
      type: String,
      default: "Alphabet Tengwar icon"
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
