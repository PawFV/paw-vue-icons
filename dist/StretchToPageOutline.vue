<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon stretch-to-page-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M20,2H4C2.89,2 2,2.89 2,4V20C2,21.11 2.89,22 4,22H20C21.11,22 22,21.11 22,20V4C22,2.89 21.11,2 20,2M20,20H4V4H20M8.83,10.25L7.29,8.71L6,10V6H10L8.71,7.29L10.25,8.83M13.75,8.83L15.29,7.29L14,6H18V10L16.71,8.71L15.17,10.25M15.17,13.75L16.71,15.29L18,14V18H14L15.29,16.71L13.75,15.17M10.25,15.17L8.71,16.71L10,18H6V14L7.29,15.29L8.83,13.75">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "StretchToPageOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Stretch To Page Outline icon"
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
