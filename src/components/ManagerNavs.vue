<template>
  <div class="admin-dashboard">
    <div class="dashboard-item" v-for="item in dashboardItems" :key="item.id">
      <button class="dashboard-button">
        <span class="icon">{{ item.icon }}</span>
        <span class="title">{{ item.title }}</span>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AdminDashboard',
  data() {
    return {
      dashboardItems: [
        { id: 1, title: '生产系统', icon: '🏭' },
        { id: 2, title: '经营系统', icon: '💼' },
        { id: 3, title: '风险系统', icon: '🌪️' },
        { id: 4, title: '项目管理', icon: '📝' },
        { id: 5, title: '人力资源', icon: '👥' },
        { id: 6, title: '财务系统', icon: '💰' },
        { id: 7, title: '数据驱动决策', icon: '📊' },
        { id: 8, title: '添加功能', icon: '➕' }
      ]
    };
  }
};
</script>

<style scoped>
.admin-dashboard {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  justify-content: center;
  padding: 20px;
}

.dashboard-item {
  width: 150px; /* adjust as needed */
  padding: 10px;
  background-color: #f0f0f0;
  border-radius: 5px;
  text-align: center;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.dashboard-button {
  border: none;
  background: none;
  padding: 10px;
  cursor: pointer;
}

.icon {
  display: block;
  font-size: 2em;
}

.title {
  display: block;
  margin-top: 5px;
}
</style>
