<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon disc-alert-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M10,14C8.89,14 8,13.1 8,12C8,10.89 8.89,10 10,10A2,2 0 0,1 12,12A2,2 0 0,1 10,14M10,4A8,8 0 0,0 2,12A8,8 0 0,0 10,20A8,8 0 0,0 18,12A8,8 0 0,0 10,4M20,12H22V7H20M20,16H22V14H20V16Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "DiscAlertIcon",
  props: {
    title: {
      type: String,
      default: "Disc Alert icon"
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
