<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon shield-plus-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M19,20V22.97H17V20H14V18H17V15H19V18H22V20H19M12,1L21,5V11C21,11.9 20.9,12.78 20.71,13.65C19.9,13.23 19,13 18,13A6,6 0 0,0 12,19C12,20.36 12.45,21.62 13.22,22.62L12,23C6.84,21.74 3,16.55 3,11V5L12,1Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "ShieldPlusIcon",
  props: {
    title: {
      type: String,
      default: "Shield Plus icon"
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
