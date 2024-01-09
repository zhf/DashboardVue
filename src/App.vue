<template>
  <div id="app" class="container mx-auto p-4">
    <h1 class="text-center text-2xl font-bold mb-4">My Dashboard</h1>
    <div class="flex flex-wrap -mx-2">
      <div class="w-full md:w-1/2 px-2 mb-4">
        <dashboard-widget class="p-4 border rounded-lg shadow"></dashboard-widget>
      </div>
      <div class="w-full md:w-1/2 px-2 mb-4">
        <sales-chart :chart-data="salesData" class="p-4 border rounded-lg shadow"></sales-chart>
      </div>
      <div class="w-full md:w-1/2 px-2 mb-4">
        <manager-navs class="p-4 border rounded-lg shadow"></manager-navs>
      </div>
      <div class="w-full md:w-1/2 px-2 mb-4">
        <website-navs class="p-4 border rounded-lg shadow"></website-navs>
      </div>
      <div class="w-full md:w-1/2 px-2 mb-4">
        <stats class="p-4 border rounded-lg shadow"></stats>
      </div>
      <div class="w-full md:w-1/2 px-2 mb-4">
        <videos class="p-4 border rounded-lg shadow"></videos>
      </div>
      <div class="w-full md:w-1/2 px-2 mb-4">
        <docs class="p-4 border rounded-lg shadow"></docs>
      </div>
      <div class="w-full md:w-1/2 px-2 mb-4">
        <news class="p-4 border rounded-lg shadow"></news>
      </div>
      <div class="w-full md:w-1/2 px-2 mb-4">
        <forum class="p-4 border rounded-lg shadow"></forum>
      </div>
      <div class="w-full md:w-1/2 px-2 mb-4">
        <announcements class="p-4 border rounded-lg shadow"></announcements>
      </div>
    </div>
  </div>
</template>

<script>
import DashboardWidget from './components/DashboardWidget.vue';
import SalesChart from './components/SalesChart.vue';
import ManagerNavs from './components/ManagerNavs.vue';
import WebsiteNavs from './components/WebsiteNavs.vue';
import Stats from './components/Stats.vue';
import Videos from './components/Videos.vue';
import Docs from './components/Docs.vue';
import News from './components/News.vue';
import Forum from './components/Forum.vue';
import Announcements from './components/Announcements.vue';

export default {
  name: 'App',
  components: {
    DashboardWidget,
    SalesChart,
    ManagerNavs,
    WebsiteNavs,
    Stats,
    Videos,
    Docs,
    News,
    Forum,
    Announcements,
  },
  data() {
    return {
      salesData: {
        labels: ['January', 'February', 'March', 'April', 'May', 'June', 'July'],
        datasets: [
          {
            label: 'Sales',
            backgroundColor: 'rgba(54, 162, 235, 0.2)',
            borderColor: 'rgba(54, 162, 235, 1)',
            borderWidth: 1,
            hoverBackgroundColor: 'rgba(54, 162, 235, 0.4)',
            hoverBorderColor: 'rgba(54, 162, 235, 1)',
            data: [6500, 5900, 8000, 8100, 5600, 5500, 4000],
            fill: false,
          }
        ]
      }
    };
  }
}
</script>

<style>
/* Add global styles here */
</style>
