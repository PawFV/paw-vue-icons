<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon relation-zero-or-one-to-zero-or-many-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M21 13L19 15H18.79A2.5 2.5 0 0 0 14.21 15H13V7H9.79A2.5 2.5 0 0 0 5.21 7H5V5H3V7H2V9H3V11H5V9H5.21A2.5 2.5 0 0 0 9.79 9H11V17H14.21A2.5 2.5 0 0 0 18.79 17H19L21 19H22V13M7.5 9A1 1 0 1 1 8.5 8A1 1 0 0 1 7.5 9M16.5 17A1 1 0 1 1 17.5 16A1 1 0 0 1 16.5 17Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "RelationZeroOrOneToZeroOrManyIcon",
  props: {
    title: {
      type: String,
      default: "Relation Zero Or One To Zero Or Many icon"
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
