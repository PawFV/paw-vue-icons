<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon surround-sound71-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M12,17A1,1 0 0,1 11,16A1,1 0 0,1 12,15A1,1 0 0,1 13,16A1,1 0 0,1 12,17M18,7V15H19V17H15V15H16V9H15L16,7H18M11,7L8,17H6L8.4,9H5V7H11Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "SurroundSound71Icon",
  props: {
    title: {
      type: String,
      default: "Surround Sound71 icon"
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
