<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon fax-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M11,6H16V8H11V6M8,9V3H19V9A3,3 0 0,1 22,12V18H19V21H8V18H7V9H8M10,5V9H17V5H10M10,15V19H17V15H10M19,11A1,1 0 0,0 18,12A1,1 0 0,0 19,13A1,1 0 0,0 20,12A1,1 0 0,0 19,11M4,9H5A1,1 0 0,1 6,10V17A1,1 0 0,1 5,18H4A2,2 0 0,1 2,16V11A2,2 0 0,1 4,9Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "FaxIcon",
  props: {
    title: {
      type: String,
      default: "Fax icon"
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
