<template>
  <div class="app-container">
    <Header />
    <div class="content">
      <Sidebar />
      <div class="breadcrumb">
        <breadcrumb/>
        <ChatList/>
        <div class="chat-section">
          <ChatConversation />
          <MediaFiles />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import Sidebar from "@/components/Sidebar.vue";
import breadcrumb from "@/components/breadcrumb.vue";
import ChatList from "@/components/ChatList.vue";
import ChatConversation from "@/components/ChatConversation.vue";
import MediaFiles from "@/components/MediaFiles.vue";

export default {
  components: { Header, Sidebar, breadcrumb, ChatList, ChatConversation, MediaFiles },
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
  background-color: white;
}

.content {
  background-color: rgb(234, 239, 240);
  display: flex;
  flex: 1;
  width: 100%;
  padding: 20px;
  margin-top: -20px;
}

.chat-section {
  display: flex;
  flex: 1;
  background-color: rgb(234, 239, 240);
  margin-top: 20px;
  }
</style>