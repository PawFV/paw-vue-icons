<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon forklift-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M6,4V11H4C2.89,11 2,11.89 2,13V17A3,3 0 0,0 5,20A3,3 0 0,0 8,17H10A3,3 0 0,0 13,20A3,3 0 0,0 16,17V13L12,4H6M17,5V19H22V17.5H18.5V5H17M7.5,5.5H11.2L14.5,13H7.5V5.5M5,15.5A1.5,1.5 0 0,1 6.5,17A1.5,1.5 0 0,1 5,18.5A1.5,1.5 0 0,1 3.5,17A1.5,1.5 0 0,1 5,15.5M13,15.5A1.5,1.5 0 0,1 14.5,17A1.5,1.5 0 0,1 13,18.5A1.5,1.5 0 0,1 11.5,17A1.5,1.5 0 0,1 13,15.5Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "ForkliftIcon",
  props: {
    title: {
      type: String,
      default: "Forklift icon"
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
