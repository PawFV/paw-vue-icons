<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon bulldozer-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M4,4A1,1 0 0,0 3,5V10C2.54,10 2.14,10.31 2.03,10.76V13.97H2.29C2.65,13.37 3.3,13 4,13H13C13.7,13 14.35,13.37 14.71,13.97H16.03L16,11V11A1,1 0 0,0 15,10H13V8A1,1 0 0,0 12,7A1,1 0 0,0 11,8V10H9V5A1,1 0 0,0 8,4H4M5,6H7V10L7,11H5V6M17,11V19H22V18L19,17L18,11H17M4,15A2,2 0 0,0 2,17A2,2 0 0,0 4,19H13A2,2 0 0,0 15,17A2,2 0 0,0 13,15H4Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "BulldozerIcon",
  props: {
    title: {
      type: String,
      default: "Bulldozer icon"
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
