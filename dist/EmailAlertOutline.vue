<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon email-alert-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M20 12V7H22V12H20M20 16V14H22V16H20M18 7C18 5.9 17.1 5 16 5H4C2.9 5 2 5.9 2 7V16C2 17.1 2.9 18 4 18H16C17.1 18 18 17.1 18 16V7M16 7L10 11L4 7H16M16 16H4V9L10 13L16 9V16Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "EmailAlertOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Email Alert Outline icon"
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
