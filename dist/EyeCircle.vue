<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon eye-circle-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M12,9.5A2.5,2.5 0 0,0 9.5,12A2.5,2.5 0 0,0 12,14.5A2.5,2.5 0 0,0 14.5,12A2.5,2.5 0 0,0 12,9.5M12,13A1,1 0 0,1 11,12A1,1 0 0,1 12,11A1,1 0 0,1 13,12A1,1 0 0,1 12,13M12,9.5A2.5,2.5 0 0,0 9.5,12A2.5,2.5 0 0,0 12,14.5A2.5,2.5 0 0,0 14.5,12A2.5,2.5 0 0,0 12,9.5M12,13A1,1 0 0,1 11,12A1,1 0 0,1 12,11A1,1 0 0,1 13,12A1,1 0 0,1 12,13M12,2A10,10 0 0,0 2,12A10,10 0 0,0 12,22A10,10 0 0,0 22,12A10,10 0 0,0 12,2M12,16C9.37,16 7,14.43 6,12C7.38,8.69 11.19,7.12 14.5,8.5C16.08,9.16 17.34,10.42 18,12C17,14.43 14.63,16 12,16M12,9.5A2.5,2.5 0 0,0 9.5,12A2.5,2.5 0 0,0 12,14.5A2.5,2.5 0 0,0 14.5,12A2.5,2.5 0 0,0 12,9.5M12,13A1,1 0 0,1 11,12A1,1 0 0,1 12,11A1,1 0 0,1 13,12A1,1 0 0,1 12,13Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "EyeCircleIcon",
  props: {
    title: {
      type: String,
      default: "Eye Circle icon"
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
