<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon credit-card-off-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M11.2 8L7.2 4H20A2 2 0 0 1 22 6V18A1.91 1.91 0 0 1 21.88 18.68L14.2 11H20V8M20.84 22.73L18.11 20H4A2 2 0 0 1 2 18V6A2 2 0 0 1 2.65 4.54L1.11 3L2.39 1.73L22.11 21.46M9.11 11L6.11 8H4V11Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "CreditCardOffIcon",
  props: {
    title: {
      type: String,
      default: "Credit Card Off icon"
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
