<template>
  <div class="forum-widget">
    <div class="forum-header">
      <h2>论坛论坛</h2>
      <span>...</span>
    </div>
    <ul class="forum-list">
      <li class="forum-item" v-for="post in forumPosts" :key="post.id">
        <div class="post-icon">
          <i class="fas fa-comment-alt"></i>
        </div>
        <div class="post-content">{{ post.content }}</div>
        <div class="post-date">{{ post.date }}</div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'ForumWidget',
  data() {
    return {
      forumPosts: [
        { id: 1, content: '这是一个帖子示例', date: '2023-05-17' },
        { id: 2, content: '示例帖子！！', date: '2023-05-17' },
        { id: 3, content: '帖子标题示例', date: '2023-05-17' },
        // More posts...
      ],
    };
  },
};
</script>

<style scoped>
.forum-widget {
  font-family: 'Arial', sans-serif;
  background: #f4f4f8;
  border-radius: 8px;
  padding: 20px;
}

.forum-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}

.forum-header h2 {
  margin: 0;
  font-size: 1.2em;
  color: #333;
}

.forum-list {
  list-style: none;
  padding: 0;
}

.forum-item {
  display: flex;
  align-items: center;
  border-bottom: 1px solid #ddd;
  padding: 10px 0;
}

.post-icon {
  color: #3498db;
  margin-right: 10px;
}

.post-content {
  flex-grow: 1;
}

.post-date {
  font-size: 0.8em;
  color: #888;
}
</style>
