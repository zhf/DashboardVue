<template>
  <div class="dashboard-widget">
    <div class="card">
      <div class="card-header">
        <h3>生产业务类</h3>
      </div>
      <ul class="list-group list-group-flush">
        <li class="list-group-item">投产次数 <span class="badge">40</span></li>
        <li class="list-group-item">勤班投计 <span class="badge">234</span></li>
        <li class="list-group-item">工程暂扣封 <span class="badge">52</span></li>
        <li class="list-group-item">早班 <span class="badge">03</span></li>
        <li class="list-group-item">满勤 <span class="badge">352</span></li>
      </ul>
    </div>
    <div class="card">
      <div class="card-header">
        <h3>生产业务类</h3>
      </div>
      <ul class="list-group list-group-flush">
        <li class="list-group-item">完成 <span class="badge">40</span></li>
        <li class="list-group-item">民商法 <span class="badge">234</span></li>
        <li class="list-group-item">刑法 <span class="badge">52</span></li>
        <li class="list-group-item">行政法 <span class="badge">03</span></li>
        <li class="list-group-item">环境保护法 <span class="badge">352</span></li>
        <li class="list-group-item">程序法 <span class="badge">52</span></li>
        <li class="list-group-item">国际法 <span class="badge">03</span></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DashboardWidget'
}
</script>

<style scoped>
.dashboard-widget {
  display: flex;
  justify-content: space-around;
}

.card {
  width: 48%;
  background-color: #f7f7f7;
  border: 1px solid #e1e1e1;
  border-radius: 4px;
}

.card-header {
  background-color: #e9ecef;
  border-bottom: 1px solid #e1e1e1;
  padding: .75rem 1.25rem;
}

.list-group-item {
  display: flex;
  justify-content: space-between;
  padding: .75rem 1.25rem;
  border: none;
}

.badge {
  display: inline-block;
  padding: .25em .4em;
  font-size: 75%;
  font-weight: 700;
  line-height: 1;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: .25rem;
  background-color: #007bff;
  color: white;
}

.card-header h3 {
  margin: 0;
}

.card + .card {
  margin-left: 1%;
}
</style>
