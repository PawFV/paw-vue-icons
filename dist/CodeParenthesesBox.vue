<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon code-parentheses-box-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M19 3H5C3.9 3 3 3.9 3 5V19C3 20.1 3.9 21 5 21H19C20.1 21 21 20.1 21 19V5C21 3.9 20.1 3 19 3M10 17.3L8.4 18C6.9 16.5 6 14.3 6 12S6.9 7.5 8.4 6L10 6.7C8.7 7.9 8 9.9 8 12S8.7 16.1 10 17.3M15.6 18L14 17.3C15.3 16 16 14.1 16 12S15.3 7.9 14 6.7L15.6 6C17.1 7.5 18 9.7 18 12C18 14.3 17.1 16.5 15.6 18Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "CodeParenthesesBoxIcon",
  props: {
    title: {
      type: String,
      default: "Code Parentheses Box icon"
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
