<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon content-save-all-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M17,7V3H7V7H17M14,17A3,3 0 0,0 17,14A3,3 0 0,0 14,11A3,3 0 0,0 11,14A3,3 0 0,0 14,17M19,1L23,5V17A2,2 0 0,1 21,19H7C5.89,19 5,18.1 5,17V3A2,2 0 0,1 7,1H19M1,7H3V21H17V23H3A2,2 0 0,1 1,21V7Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "ContentSaveAllIcon",
  props: {
    title: {
      type: String,
      default: "Content Save All icon"
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
