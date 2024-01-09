<template>
  <div class="news-widget">
    <div class="news-item" v-for="news in newsData" :key="news.id">
      <div class="news-date">{{ news.date }}</div>
      <div class="news-content">{{ news.content }}</div>
      <div class="news-status" v-if="news.hot">
        <span class="hot-news">HOT</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NewsWidget',
  data() {
    return {
      newsData: [
        { id: 1, date: '2023-05-17', content: '这是一条新闻的示例内容1', hot: true },
        { id: 2, date: '2023-05-17', content: '这是一条新闻的示例内容2', hot: false },
        { id: 3, date: '2023-05-17', content: '这是一条新闻的示例内容3', hot: true },
        { id: 4, date: '2023-05-17', content: '这是一条新闻的示例内容4', hot: false },
      ],
    };
  },
};
</script>

<style scoped>
.news-widget {
  font-family: 'Arial', sans-serif;
}

.news-item {
  border-bottom: 1px solid #ccc;
  padding: 10px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.news-date {
  font-size: 0.8em;
  color: #888;
}

.news-content {
  flex-grow: 1;
  padding: 0 15px;
}

.hot-news {
  color: #ff4500;
  font-weight: bold;
}
</style>
