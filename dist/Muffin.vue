<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon muffin-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M16,5C16,5 15,2 12,2C9,2 8,5 8,5C6,5 4,7 4,9C1.3,9 1.3,13 4,13H20C22.7,13 22.7,9 20,9C20,7 18,5 16,5M5,15L7,22H9L8,15H5M10,15L11,22H13L14,15H10M16,15L15,22H17L19,15H16Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "MuffinIcon",
  props: {
    title: {
      type: String,
      default: "Muffin icon"
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
