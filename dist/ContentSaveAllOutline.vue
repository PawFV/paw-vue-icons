<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon content-save-all-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M1 7H3V21H17V23H3C1.9 23 1 22.11 1 21V7M19 1H7C5.89 1 5 1.9 5 3V17C5 18.1 5.89 19 7 19H21C22.1 19 23 18.1 23 17V5L19 1M21 17H7V3H18.17L21 5.83V17M14 10C12.34 10 11 11.34 11 13S12.34 16 14 16 17 14.66 17 13 15.66 10 14 10M8 4H17V8H8V4Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "ContentSaveAllOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Content Save All Outline icon"
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
