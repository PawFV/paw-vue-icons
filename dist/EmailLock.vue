<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon email-lock-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M20.5,0A2.5,2.5 0 0,1 23,2.5V3A1,1 0 0,1 24,4V8A1,1 0 0,1 23,9H18A1,1 0 0,1 17,8V4A1,1 0 0,1 18,3V2.5A2.5,2.5 0 0,1 20.5,0M12,11L4,6V8L12,13L16.18,10.39C16.69,10.77 17.32,11 18,11H22V18A2,2 0 0,1 20,20H4A2,2 0 0,1 2,18V6A2,2 0 0,1 4,4H15V8C15,8.36 15.06,8.7 15.18,9L12,11M20.5,1A1.5,1.5 0 0,0 19,2.5V3H22V2.5A1.5,1.5 0 0,0 20.5,1Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "EmailLockIcon",
  props: {
    title: {
      type: String,
      default: "Email Lock icon"
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
