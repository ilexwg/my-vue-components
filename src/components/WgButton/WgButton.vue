<template>
  <button class="wg-button"
    @click="onClick"
    :class="[type ? 'wg-button--' + type : '', {'is-round': round}]">
    <slot></slot>
  </button>
</template>

<script>
export default {
  props: {
    type: {
      type: String,
      default: 'default'
    },
    round: Boolean
  },
  methods: {
    onClick() {
      this.$emit('click');
    }
  }
};
</script>

<style lang="less" scoped>
.wg-button {
  line-height: 1;
  padding: 12px 20px;
  outline: none;
  border: 1px solid #666;
  border-radius: 4px;
  font-size: 14px;
  background-color: #fff;
  color: #666;
  transition: 0.1s;
  cursor: pointer;
  &:hover {
    background-color: #eee;
  }
}

.wg-button+.wg-button {
  margin-left: 10px;
}

.is-round {
  border-radius: 20px;
  padding: 12px 23px;
}

.wg-button--danger {
  background-color: #900;
  color: #fff;
}
</style>
