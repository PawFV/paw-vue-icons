<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon bookmark-off-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M3.28,4L2,5.27L5,8.27V21L12,18L16.78,20.05L18.73,22L20,20.72L3.28,4M7,18V10.27L13,16.25L12,15.82L7,18M7,5.16L5.5,3.67C5.88,3.26 6.41,3 7,3H17A2,2 0 0,1 19,5V17.16L17,15.16V5H7V5.16Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "BookmarkOffOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Bookmark Off Outline icon"
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
