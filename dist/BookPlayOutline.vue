<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon book-play-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M17,16L22,19L17,22V16M18,2A2,2 0 0,1 20,4V15.42L18,14.27V4H13V12L10.5,9.75L8,12V4H6V20H15V22H6A2,2 0 0,1 4,20V4A2,2 0 0,1 6,2H18Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "BookPlayOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Book Play Outline icon"
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
