<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon elephant-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M19.5,15.5A0.5,0.5 0 0,1 19,16A0.5,0.5 0 0,1 18.5,15.5V8.5C18.5,6.57 16.43,5 14.5,5H6A4,4 0 0,0 2,9V19H6V15H11V19H15V14.5A0.5,0.5 0 0,1 15.5,14A0.5,0.5 0 0,1 16,14.5V16A3,3 0 0,0 19,19A3,3 0 0,0 22,16V14H19.5V15.5Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "ElephantIcon",
  props: {
    title: {
      type: String,
      default: "Elephant icon"
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
