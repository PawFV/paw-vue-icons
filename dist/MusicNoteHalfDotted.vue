<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon music-note-half-dotted-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M14 3H12V13.56A3.96 3.96 0 0 0 10 13A4 4 0 1 0 14 17V3M10 19A2 2 0 1 1 12 17A2 2 0 0 1 10 19M16.5 20A1.5 1.5 0 1 1 18 18.5A1.5 1.5 0 0 1 16.5 20Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "MusicNoteHalfDottedIcon",
  props: {
    title: {
      type: String,
      default: "Music Note Half Dotted icon"
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
