<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon currency-gbp-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M6,21V19C10,17 9.5,13 9.5,13H7V11H9.5C8.5,6.5 10,3 14,3C16,3 17,3.5 17,3.5V5.5C11,3.5 11,8 11.5,11H16V13H11.5C11.5,13 12,17 9.5,19H18V21H6Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "CurrencyGbpIcon",
  props: {
    title: {
      type: String,
      default: "Currency Gbp icon"
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
