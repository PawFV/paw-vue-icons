<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon oil-lamp-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M5,20H16V22H5M11,5H10A2,2 0 0,0 8,7H13A2,2 0 0,0 11,5M16,8H22A2,2 0 0,1 20,10H19A4,4 0 0,0 15,14V15A4,4 0 0,1 11,19H10A4,4 0 0,1 6,15H4A2,2 0 0,1 2,13V10A2,2 0 0,1 4,8M6,10H4V13H6M19,5A2,2 0 0,1 21,7H22A2.9,2.9 0 0,0 19,4A2,2 0 0,1 17,2H16A2.9,2.9 0 0,0 19,5">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "OilLampIcon",
  props: {
    title: {
      type: String,
      default: "Oil Lamp icon"
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
