<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon dots-vertical-circle-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M2,12A10,10 0 0,1 12,2A10,10 0 0,1 22,12A10,10 0 0,1 12,22A10,10 0 0,1 2,12M10.5,12A1.5,1.5 0 0,0 12,13.5A1.5,1.5 0 0,0 13.5,12A1.5,1.5 0 0,0 12,10.5A1.5,1.5 0 0,0 10.5,12M10.5,17.5A1.5,1.5 0 0,0 12,19A1.5,1.5 0 0,0 13.5,17.5A1.5,1.5 0 0,0 12,16A1.5,1.5 0 0,0 10.5,17.5M10.5,6.5A1.5,1.5 0 0,0 12,8A1.5,1.5 0 0,0 13.5,6.5A1.5,1.5 0 0,0 12,5A1.5,1.5 0 0,0 10.5,6.5Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "DotsVerticalCircleIcon",
  props: {
    title: {
      type: String,
      default: "Dots Vertical Circle icon"
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
