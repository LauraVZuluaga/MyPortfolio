<template>
  <div>
    <button
      :type="type"
      :class="extraClass"
      v-on:click="clicked"
      :title="title"
      :disabled="disabled"
    >
      <template v-if="icon">
        <i class="material-icons">{{ icon }}</i>
      </template>
      <template v-if="loading">
        <app-loader />
      </template>
      <template v-else>
        <slot></slot>
      </template>
    </button>
  </div>
</template>

<script>
export default {
  name: "app-button",
  props: {
    extraClass: { type: String, required: false },
    loading: { type: Boolean, required: false, default: false },
    icon: { type: String, required: false },
    title: { type: String, required: false },
    type: { type: String, required: false, default: "button" },
    disabled: { type: Boolean, required: false, default: false },
  },
  data() {
    return {};
  },
  methods: {
    clicked() {
      this.$emit("click");
    },
  },
};
</script>

<style lang="scss">
@import "@/assets/style.scss";

button {
  font-family: inherit;
  user-select: none;
}
</style>
