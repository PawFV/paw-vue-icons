<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon stretch-to-page-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M20,2H4C2.89,2 2,2.89 2,4V20C2,21.11 2.89,22 4,22H20C21.11,22 22,21.11 22,20V4C22,2.89 21.11,2 20,2M9,19H5V15L6.29,16.29L7.83,14.75L9.25,16.17L7.71,17.71M7.83,9.25L6.29,7.71L5,9V5H9L7.71,6.29L9.25,7.83M19,19H15L16.29,17.71L14.75,16.17L16.17,14.75L17.71,16.29L19,15M19,9L17.71,7.71L16.17,9.25L14.75,7.83L16.29,6.29L15,5H19">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "StretchToPageIcon",
  props: {
    title: {
      type: String,
      default: "Stretch To Page icon"
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
