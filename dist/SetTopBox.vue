<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon set-top-box-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M5,15.5A0.5,0.5 0 0,1 4.5,16H3.5A0.5,0.5 0 0,1 3,15.5V15H2A1,1 0 0,1 1,14V11A1,1 0 0,1 2,10H22A1,1 0 0,1 23,11V14A1,1 0 0,1 22,15H21V15.5A0.5,0.5 0 0,1 20.5,16H19.5A0.5,0.5 0 0,1 19,15.5V15H5V15.5M3,12V13H5V12H3M6,12V13H8V12H6M20.5,11.5A1,1 0 0,0 19.5,12.5A1,1 0 0,0 20.5,13.5A1,1 0 0,0 21.5,12.5A1,1 0 0,0 20.5,11.5Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "SetTopBoxIcon",
  props: {
    title: {
      type: String,
      default: "Set Top Box icon"
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
