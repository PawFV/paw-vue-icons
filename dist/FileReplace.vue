<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon file-replace-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M14,12H19.5L14,6.5V12M8,5H15L21,11V21A2,2 0 0,1 19,23H8C6.89,23 6,22.1 6,21V18H11V20L15,17L11,14V16H6V7A2,2 0 0,1 8,5M13.5,3H4V16H6V18H4A2,2 0 0,1 2,16V3A2,2 0 0,1 4,1H11.5L13.5,3Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "FileReplaceIcon",
  props: {
    title: {
      type: String,
      default: "File Replace icon"
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
