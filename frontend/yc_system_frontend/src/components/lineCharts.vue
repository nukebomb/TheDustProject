<template>
  <div id="linemain"></div>
</template>

<script>
export default {
  name: 'lineCharts',
  data() {
    return {
    }
  },
  mounted() {
    var linechart = this.echarts.init(document.getElementById('linemain'))
    linechart.setOption({
      xAxis: {
        type: 'category',
        data: ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun']
      },
      yAxis: {
        type: 'value'
      },
      series: [{
        data: [820, 932, 901, 934, 1290, 1330, 1320],
        type: 'line'
      }]
    })
  }
}
</script>

<style>
#linemain {
  width: 100%;
  height: 100%;
}
</style>
