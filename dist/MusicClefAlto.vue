<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon music-clef-alto-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M5 4H7V20H5M15.46 13H14.83L13.83 12L14.83 11H15.46A3.5 3.5 0 1 0 11.96 7.5H13.96A1.5 1.5 0 1 1 15.46 9H14L12 11H11V4H9V20H11V13H12L14 15H15.46A1.5 1.5 0 1 1 13.96 16.5H11.96A3.5 3.5 0 1 0 15.46 13Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "MusicClefAltoIcon",
  props: {
    title: {
      type: String,
      default: "Music Clef Alto icon"
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
