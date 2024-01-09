<template>
  <div class="dashboard-widget">
    <div class="widget-header">
      <h1>指标统计</h1>
    </div>
    <div class="widget-content">
      <div class="stat-item">
        <span class="stat-title">本年开单(个)</span>
        <span class="stat-value">200</span>
      </div>
      <div class="stat-item">
        <span class="stat-title">本年完成(个)</span>
        <span class="stat-value">300</span>
      </div>
      <div class="stat-item">
        <span class="stat-title">本年完成(个)</span>
        <span class="stat-value">300</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DashboardWidget',
  data() {
    return {
      // Mock data for the dashboard widget
      stats: [
        { title: '本年开单(个)', value: 200 },
        { title: '本年完成(个)', value: 300 },
        { title: '本年完成(个)', value: 300 }
      ]
    };
  }
}
</script>

<style scoped>
.dashboard-widget {
  font-family: 'Arial', sans-serif;
  color: #333;
}

.widget-header h1 {
  font-size: 1.5em;
  color: #ff6f00;
}

.widget-content {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.stat-item {
  margin: 10px 0;
}

.stat-title {
  font-size: 1em;
  margin-right: 5px;
}

.stat-value {
  font-size: 1.2em;
  font-weight: bold;
}
</style>