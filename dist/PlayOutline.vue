<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon play-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M8.5,8.64L13.77,12L8.5,15.36V8.64M6.5,5V19L17.5,12">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "PlayOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Play Outline icon"
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
