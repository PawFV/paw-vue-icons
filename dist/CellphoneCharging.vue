<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon cellphone-charging-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M11 18.5V13H9L13 5.5V11H15M17 19H7V5H17M17 1H7C5.89 1 5 1.89 5 3V21A2 2 0 0 0 7 23H17A2 2 0 0 0 19 21V3C19 1.89 18.1 1 17 1Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "CellphoneChargingIcon",
  props: {
    title: {
      type: String,
      default: "Cellphone Charging icon"
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
