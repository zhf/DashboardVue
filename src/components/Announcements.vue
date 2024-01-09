<template>
  <div class="announcement-widget">
    <div class="announcement-header">
      <h2>集团公告</h2>
      <span>...</span>
    </div>
    <div class="announcement-feature">
      <img src="https://placehold.co/600x400" alt="Featured Image" class="feature-image"/>
      <div class="feature-content">
        <h3>2023年全国优秀示范水电工程勘测设计资格申报团队公示</h3>
        <p class="feature-date">2023-04-20</p>
        <p class="feature-excerpt">这是公告内容的简短摘要，公告的详细内容摘要可以放在这里，公告的详细内容摘要可以放在这里。</p>
      </div>
    </div>
    <ul class="announcement-list">
      <li v-for="item in announcements" :key="item.id">
        <i class="bullet-icon fas fa-circle"></i>
        <span class="announcement-title">{{ item.title }}</span>
        <span class="announcement-date">{{ item.date }}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'AnnouncementWidget',
  data() {
    return {
      announcements: [
        { id: 1, title: '长江设计集团下属事务所招聘', date: '2023-04-20' },
        { id: 2, title: '职工食堂“五一”劳动节招标通知', date: '2023-04-20' },
        { id: 3, title: '关于2023年劳动节放假通知事项的通知', date: '2023-04-20' },
        { id: 4, title: '长江设计集团举办“五一”健康跑活动的通知', date: '2023-04-20' },
      ],
    };
  },
};
</script>

<style scoped>
.announcement-widget {
  font-family: 'Arial', sans-serif;
  background: #f9f9f9;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.announcement-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 16px;
  background: #e5e5e5;
  border-bottom: 1px solid #d1d1d1;
}

.announcement-header h2 {
  font-size: 1.25rem;
  color: #333;
  margin: 0;
}

.announcement-feature {
  display: flex;
  padding: 16px;
  border-bottom: 1px solid #d1d1d1;
}

.feature-image {
  width: 120px;
  height: 90px;
  object-fit: cover;
  margin-right: 16px;
  border-radius: 4px;
}

.feature-content h3 {
  font-size: 1rem;
  color: #333;
  margin: 0 0 8px 0;
}

.feature-content .feature-date {
  font-size: 0.85rem;
  color: #666;
}

.feature-content .feature-excerpt {
  font-size: 0.85rem;
  color: #666;
  margin: 0;
}

.announcement-list {
  list-style: none;
  padding: 0;
  margin: 0;
}

.announcement-item {
  display: flex;
  align-items: center;
  padding: 8px 16px;
}

.bullet-icon {
  color: #3498db;
  font-size: 0.5rem;
  margin-right: 8px;
}

.announcement-title {
  flex-grow: 1;
  font-size: 0.85rem;
}

.announcement-date {
  font-size: 0.75rem;
  color: #999;
}
</style>
