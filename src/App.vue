<template>
  <div class="app-container">
    <Header />
    <div class="content">
      <Sidebar />
      <div class="chat-section">
        <ChatList />
        <ChatConversation />
      </div>
      <MediaFiles />
    </div>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import Sidebar from "@/components/Sidebar.vue";
import ChatList from "@/components/ChatList.vue";
import ChatConversation from "@/components/ChatConversation.vue";
import MediaFiles from "@/components/MediaFiles.vue";

export default {
  components: { Header, Sidebar, ChatList, ChatConversation, MediaFiles },
};

</script>

<style scoped>

html, body {
  overflow-x: hidden;
  margin: 0;
  padding: 0;
  width: 100%;
}

.app-container {
  display: flex;
  flex-direction: column;
  width: 100vw;
  height: 100vh;
  background-color: #f8f9fa;
}

.content {
  display: flex;
  flex: 1;
  margin-top: 60px; 
  width: 100%;
}

.chat-section {
  display: flex;
  flex: 1;
  background-color: white;
  border-left: 1px solid #e9ecef;
  border-right: 1px solid #e9ecef;
}
</style>