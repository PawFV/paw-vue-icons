<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon playlist-music-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M15,6V8H3V6H15M15,10V12H3V10H15M3,16V14H11V16H3M17,6H22V8H19V17A3,3 0 0,1 16,20A3,3 0 0,1 13,17A3,3 0 0,1 16,14C16.35,14 16.69,14.07 17,14.18V6M16,16A1,1 0 0,0 15,17A1,1 0 0,0 16,18A1,1 0 0,0 17,17A1,1 0 0,0 16,16Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "PlaylistMusicOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Playlist Music Outline icon"
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
