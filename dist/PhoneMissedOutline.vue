<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon phone-missed-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M18.6 15.5v1.8c.7.4 1.3.8 1.9 1.3l1.1-1.1c-.9-.9-1.9-1.5-3-2m-13.2 0c-1 .5-2 1.1-2.9 1.9l1.1 1.1c.6-.5 1.2-.9 1.9-1.3v-1.7M12 12c4.5 0 8.7 1.7 11.7 4.7.2.2.3.4.3.7 0 .3-.1.5-.3.7l-2.5 2.5c-.2.2-.4.3-.7.3-.2 0-.5-.1-.7-.3-.8-.7-1.7-1.4-2.7-1.8-.3-.2-.6-.5-.6-.9v-3.1c-1.5-.5-3-.7-4.6-.7-1.6 0-3.1.2-4.6.7v3.1c0 .4-.2.7-.6.9-1 .5-1.9 1.1-2.7 1.8-.2.2-.4.3-.7.3-.3 0-.5-.1-.7-.3L.1 18.1c0-.2-.1-.5-.1-.7 0-.3.1-.5.3-.7C3.3 13.8 7.5 12 12 12zM6.5 5.5V9H5V3h6v1.5H7.5L12 9l6-6 1 1-7 7-5.5-5.5z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "PhoneMissedOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Phone Missed Outline icon"
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
