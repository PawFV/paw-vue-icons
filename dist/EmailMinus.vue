<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon email-minus-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M3,4C1.89,4 1,4.89 1,6V18A2,2 0 0,0 3,20H14.09C14.03,19.67 14,19.34 14,19A6,6 0 0,1 20,13C20.34,13 20.67,13.03 21,13.09V6C21,4.89 20.1,4 19,4H3M3,6L11,11L19,6V8L11,13L3,8V6M16,18V20H24V18H16Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "EmailMinusIcon",
  props: {
    title: {
      type: String,
      default: "Email Minus icon"
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
