<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon vhs-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M4,6A2,2 0 0,0 2,8V16A2,2 0 0,0 4,18H20A2,2 0 0,0 22,16V8A2,2 0 0,0 20,6H4M4.54,10H7V14H4.54C4.19,13.39 4,12.7 4,12C4,11.3 4.19,10.61 4.54,10M9,10H15V14H9V10M17,10H19.46C19.81,10.61 20,11.3 20,12C20,12.7 19.81,13.39 19.46,14H17V10Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "VhsIcon",
  props: {
    title: {
      type: String,
      default: "Vhs icon"
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
