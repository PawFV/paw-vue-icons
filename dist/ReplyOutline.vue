<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon reply-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M8,9.8V10.7L9.7,11C12.3,11.4 14.2,12.4 15.6,13.7C13.9,13.2 12.1,12.9 10,12.9H8V14.2L5.8,12L8,9.8M10,5L3,12L10,19V14.9C15,14.9 18.5,16.5 21,20C20,15 17,10 10,9">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "ReplyOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Reply Outline icon"
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
