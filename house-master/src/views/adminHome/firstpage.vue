<template>
  <div>
    <div id="main" style="width: 1000px; height: 800px"></div>
    <!-- 这里可以添加一些默认显示的内容，或者直接留空 -->
  </div>
</template>

<script>
import * as echarts from "echarts";

export default {
  data() {
    return {
      // 移除了 aa, option 等不需要的内容
      loading: false,
      error: ''
    };
  },
  created() {
    // 如果不需要请求数据和初始化图表，这里可以注释掉调用
    // this.cityCountEstate();
  },
  methods: {
    // 若不需要请求数据的方法，也可以将其删除
    cityCountEstate() {
      this.loading = true;
      this.error = '';
      // request({ url: "count", method: "get" })
      //   .then((resp) => {
      //     // 由于移除了 option，这里的代码不再适用
      //     // this.option.series[0].data = resp.data.data;
      //     // console.log(this.option.series[0].data);
      //     // var myChart = echarts.init(document.getElementById("main"));
      //     // myChart.setOption(this.option, true);
      //     this.loading = false;
      //   })
      //   .catch((error) => {
      //     if (error.response) {
      //       this.error = `服务器响应错误: ${error.response.status} - ${error.response.data}`;
      //     } else if (error.request) {
      //       this.error = '请求未收到响应，请检查网络或服务器';
      //     } else {
      //       this.error = `请求出错: ${error.message}`;
      //     }
      //     this.loading = false;
      //   });
    }
  }
};
</script>

<style>
</style>