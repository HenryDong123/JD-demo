<!--
 * @Description: 
 * @Date: 2019-06-25 18:16:21
 * @LastEditors: HenryDong
 * @LastEditTime: 2019-06-28 10:46:21
 -->
<!-- 组件说明 -->
<template>
  <section :class="[panleClass,cname]">
    <h4>-{{ title }}-</h4>
    <slot/>
  </section>
</template>
<script>
export default {
  components: {},
  props: {
    cname: {
      type: String,
      default: ""
    },
    title: {
        type: String,
        default: ''
    }
  },
  data() {
    return {
      panleClass: "panel"
    };
  },
  computed: {},
  methods: {}
};
</script>

<style lang='scss' scoped>
@import "../../css/element.scss";
.panel{
    @include panel;
}
</style>
