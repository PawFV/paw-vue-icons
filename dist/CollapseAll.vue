<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon collapse-all-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M14,4H4V14H2V4A2,2 0 0,1 4,2H14V4M18,6H8A2,2 0 0,0 6,8V18H8V8H18V6M22,12V20A2,2 0 0,1 20,22H12A2,2 0 0,1 10,20V12A2,2 0 0,1 12,10H20A2,2 0 0,1 22,12M20,15H12V17H20V15Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "CollapseAllIcon",
  props: {
    title: {
      type: String,
      default: "Collapse All icon"
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
