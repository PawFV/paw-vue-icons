<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon rivet-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M11.43,2C10.61,2 9.94,2.65 9.94,3.5C9.94,4.64 9.94,5.8 9.94,6.96H7.95V7.95H15.91V6.96H13.92C13.92,5.8 13.92,4.64 13.92,3.5C13.92,2.65 13.25,2 12.43,2H11.43M10.94,8.95V21.87L11.93,22.87L12.92,21.87V8.95H10.94Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "RivetIcon",
  props: {
    title: {
      type: String,
      default: "Rivet icon"
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
