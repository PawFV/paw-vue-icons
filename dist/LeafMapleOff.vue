<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon leaf-maple-off-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M18.11 14.91L8.2 5H10L12 2L14 5H16L14.37 9.9L17.79 6L18.79 7.73L22.39 7.96L20.79 11.19L21.79 13L18.11 14.91M2.39 1.73L1.11 3L5.45 7.34L5.21 7.77L1.61 8L3.21 11.27L2.21 13L8 16L7 18L11 17.25V21H13V17.25L15.91 17.8L20.84 22.73L22.11 21.46L2.39 1.73Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "LeafMapleOffIcon",
  props: {
    title: {
      type: String,
      default: "Leaf Maple Off icon"
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
