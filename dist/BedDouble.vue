<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon bed-double-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M18 10V7A2 2 0 0 0 16 5H8A2 2 0 0 0 6 7V10A2 2 0 0 0 4 12V17H5.33L6 19H7L7.67 17H16.33L17 19H18L18.67 17H20V12A2 2 0 0 0 18 10M11 10H8V7H11M16 10H13V7H16Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "BedDoubleIcon",
  props: {
    title: {
      type: String,
      default: "Bed Double icon"
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
