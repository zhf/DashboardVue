<template>
  <div class="video-dashboard-widget">
    <div class="video-list">
      <div v-for="(video, index) in videos" :key="index" class="video-item">
        <div class="thumbnail-wrapper">
          <img :src="video.thumbnail" class="thumbnail" />
          <div class="play-icon">&#9658;</div>
        </div>
        <div class="video-info">
          <div class="title">{{ video.title }}</div>
          <div class="date">{{ video.date }}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'VideoDashboardWidget',
  data() {
    return {
      videos: [
        // Mockup data based on the screenshot provided
        { thumbnail: 'https://placehold.co/600x400', title: '人民网访谈', date: '05-19' },
        { thumbnail: 'https://placehold.co/600x400', title: '国家记忆', date: '05-19' },
        { thumbnail: 'https://placehold.co/600x400', title: '经济如何控制提质增效', date: '05-19' },
        { thumbnail: 'https://placehold.co/600x400', title: '集团PMC的角色', date: '05-19' }
      ]
    }
  }
}
</script>

<style scoped>
.video-dashboard-widget {
  max-width: 400px;
  margin: auto;
}

.video-list {
  display: flex;
  flex-direction: column;
}

.video-item {
  display: flex;
  margin-bottom: 10px;
}

.thumbnail-wrapper {
  position: relative;
  margin-right: 10px;
}

.thumbnail {
  width: 80px;
  height: 60px;
  object-fit: cover;
}

.play-icon {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: white;
  font-size: 24px;
}

.video-info {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.title {
  font-size: 14px;
  color: #333;
}

.date {
  font-size: 12px;
  color: #666;
}
</style>
