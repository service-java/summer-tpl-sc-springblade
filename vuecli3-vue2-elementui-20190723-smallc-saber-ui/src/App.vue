<template>
  <div id="app">
    <router-view />
  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {};
  },
  watch: {},
  created() {
    this.$notify.success({
      title: "授权信息",
      dangerouslyUseHTMLString: true,
      message:
        '<p>欢迎使用Saber!</p>' +
        '<p>该系统采用BladeX与AvueX开发，</p>' +
        '<p>若要商用强烈推荐高度定制的商业化框架，具体授权信息请访问如下地址。️</p>' +
        '</br>' +
        '<p>BladeX 授权地址：<a target="_blank" href="https://bladex.vip/#/vip">点击授权</a></p>' +
        '<p>AvueX 授权地址：<a target="_blank" href="https://avuex.avue.top/#/vip">点击授权</a></p>',
      duration: 20000,
      type: "success"
    });
    setTimeout(()=>{
      this.$notify.success({
        title: "开发手册",
        dangerouslyUseHTMLString: true,
        message:
          '<p>后端开发手册：<a target="_blank" href="https://www.kancloud.cn/smallchill/blade">点击查看</a></p>'+
          '<p>前端开发手册：<a target="_blank" href="https://www.kancloud.cn/smallwei/avue">点击查看</a></p>',
        duration: 20000,
        type: "success"
      });
    },500);
  },
  methods: {},
  computed: {}
};
</script>
<style lang="scss">
#app {
  width: 100%;
  height: 100%;
  overflow: hidden;
}
</style>
