<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon folder-multiple-plus-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M22 4C23.1 4 24 4.9 24 6V16C24 17.1 23.1 18 22 18H6C4.9 18 4 17.1 4 16V4C4 2.9 4.9 2 6 2H12L14 4H22M2 6V20H20V22H2C.9 22 0 21.1 0 20V6H2M6 6V16H22V6H6M14 10H16V8H18V10H20V12H18V14H16V12H14V10Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "FolderMultiplePlusOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Folder Multiple Plus Outline icon"
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
