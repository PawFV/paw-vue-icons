<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon symbol-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M2 7V14H4V7H2M6 7V9H10V11H8V14H10V13C11.11 13 12 12.11 12 11V9C12 7.89 11.11 7 10 7H6M15.8 7L15.6 9H14V11H15.4L15.2 13H14V15H15L14.8 17H16.8L17 15H18.4L18.2 17H20.2L20.4 15H22V13H20.6L20.8 11H22V9H21L21.2 7H19.2L19 9H17.6L17.8 7H15.8M17.4 11H18.8L18.6 13H17.2L17.4 11M2 15V17H4V15H2M8 15V17H10V15H8Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "SymbolIcon",
  props: {
    title: {
      type: String,
      default: "Symbol icon"
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
