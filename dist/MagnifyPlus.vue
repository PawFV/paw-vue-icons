<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon magnify-plus-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M9,2A7,7 0 0,1 16,9C16,10.57 15.5,12 14.61,13.19L15.41,14H16L22,20L20,22L14,16V15.41L13.19,14.61C12,15.5 10.57,16 9,16A7,7 0 0,1 2,9A7,7 0 0,1 9,2M8,5V8H5V10H8V13H10V10H13V8H10V5H8Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "MagnifyPlusIcon",
  props: {
    title: {
      type: String,
      default: "Magnify Plus icon"
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
