<!-- 组件说明 -->
<template>
  <div :class="[btnClass,cname]">
    <slot/>
  </div>
</template>

<script>
//import x from ''
export default {
  props: {
    cname: {
      type: String,
      default: ""
    }
  },
  components: {},
  data() {
    return {
      btnClass: "btn"
    };
  },
  computed: {},
  methods: {}
};
</script>

<style lang='scss' scoped>
@import '../../css/element.scss';
.btn {
    @include btn;
}
</style>