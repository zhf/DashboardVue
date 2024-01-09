<template>
  <div class="special-topic-container">
    <button class="special-topic-button">
      {{ buttonText }}
      <span class="arrow-right">→</span>
    </button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      // Replace 'Special Topic A' with actual button text if needed
      buttonText: '专题网站专题网站A'
    }
  }
}
</script>

<style scoped>
.special-topic-container {
  /* Add container styles here */
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: blue; /* Replace with actual color code */
  height: 50px; /* Adjust as needed */
}

.special-topic-button {
  /* Add button styles here */
  background-color: white; /* Replace with actual color code */
  border: none;
  cursor: pointer;
  display: flex;
  align-items: center;
  padding: 10px 20px; /* Adjust as needed */
}

.arrow-right {
  /* Style for the arrow, adjust as needed */
  margin-left: 10px;
}
</style>
