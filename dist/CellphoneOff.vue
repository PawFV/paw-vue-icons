<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon cellphone-off-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M2.38,1.73L1.11,3L5,6.89V21A2,2 0 0,0 7,23H17A2,2 0 0,0 19,21V20.89L20.84,22.73L22.11,21.46M17,19H7V8.89L17,18.89V19M17,5V13.8L19,15.8V3A2,2 0 0,0 17,1H7C6.28,1 5.6,1.37 5.24,2L8.24,5H17Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "CellphoneOffIcon",
  props: {
    title: {
      type: String,
      default: "Cellphone Off icon"
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
