<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon bolt-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M14,17.7V21H10V20.3L14,17.7M17,3H7V6H17V3M15,7L14,7.7V7H10V10.3L9,11V12L15,8.1V7M15,11L14,11.7V9.7L10,12.4V14.4L9,15V16L15,12.1V11M15,15L14,15.7V13.7L10,16.4V18.4L9,19V20L15,16.1V15Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "BoltIcon",
  props: {
    title: {
      type: String,
      default: "Bolt icon"
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
