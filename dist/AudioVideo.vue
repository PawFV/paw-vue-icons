<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon audio-video-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M20,7H4A2,2 0 0,0 2,9V15A2,2 0 0,0 4,17H5V18C5,18.6 5.4,19 6,19H8C8.6,19 9,18.6 9,18V17H15V18C15,18.6 15.4,19 16,19H18C18.6,19 19,18.6 19,18V17H20A2,2 0 0,0 22,15V9A2,2 0 0,0 20,7M14,12H4V10H14V12M18,13A2,2 0 0,1 16,11A2,2 0 0,1 18,9A2,2 0 0,1 20,11A2,2 0 0,1 18,13M6,15H4V14H6V15M10,15H8V14H10V15M14,15H12V14H14V15Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "AudioVideoIcon",
  props: {
    title: {
      type: String,
      default: "Audio Video icon"
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
