<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon mailbox-open-up-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M14,12.85V6.85H18V8.85H16V12.85H14M18,3.85H8A5,5 0 0,0 3,8.85V17.85H1V19.85H21A2,2 0 0,0 23,17.85V8.85A5,5 0 0,0 18,3.85M11,17.85H5V8.85A3,3 0 0,1 8,5.85A3,3 0 0,1 11,8.85V17.85M21,17.85H13V8.85C13,7.76 12.65,6.71 12,5.85H18A3,3 0 0,1 21,8.85V17.85Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "MailboxOpenUpOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Mailbox Open Up Outline icon"
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
