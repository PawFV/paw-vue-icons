<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon table-column-width-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M5,8H19A2,2 0 0,1 21,10V20A2,2 0 0,1 19,22H5A2,2 0 0,1 3,20V10A2,2 0 0,1 5,8M5,12V15H11V12H5M13,12V15H19V12H13M5,17V20H11V17H5M13,17V20H19V17H13M11,2H21V6H19V4H13V6H11V2Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "TableColumnWidthIcon",
  props: {
    title: {
      type: String,
      default: "Table Column Width icon"
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
