<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon globe-light-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M13 8.08V2H11V8.08C7.61 8.57 5 11.47 5 15C5 18.87 8.13 22 12 22S19 18.87 19 15C19 11.47 16.39 8.57 13 8.08M12 20C9.24 20 7 17.76 7 15C7 13.87 7.39 12.84 8.03 12H15.97C16.61 12.84 17 13.87 17 15C17 17.76 14.76 20 12 20Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "GlobeLightIcon",
  props: {
    title: {
      type: String,
      default: "Globe Light icon"
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
