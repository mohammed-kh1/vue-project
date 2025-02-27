<template>
  <div class="chatconversation col-12 col-md-8 p-3" style="background-color: white; position: relative;">
    <div class="d-flex justify-content-between align-items-center mb-3 border-bottom" style="padding-bottom: 10px;">
      <h2 class="text-lg fw-bold mb-0" style="color: #333;"></h2>
      <div>
        <button class="btn btn-sm me-2" @click="showBlock = true">
          <img src="/slash.png" alt="slash icon" />
        </button>
        <button class="btn btn-sm me-2" @click="showDelete = true">
          <img src="/Vector.png" alt="red trash icon" />
        </button>
        <button class="btn btn-sm me-2">
          <img src="/call.png" alt="call icon" /> 
        </button>
        <button class="btn btn-sm me-2">
          <img src="/video1.png" alt="video icon" />
        </button>
        <button class="btn btn-sm me-2" @click="showListsPopup = true">
          <img src="/lists.png" alt="list icon" />
        </button>
      </div>
    </div>
    <div class="chat-container h-[calc(100vh-200px)] overflow-y-auto border-bottom">
      <div v-for="message in messages" :key="message.id" class="mb-3 p-2">
        <div class="d-flex align-items-start" :class="{ 'flex-row-reverse': message.isSender }">
          <img :src="message.avatar" class="rounded-circle" style="width: 40px; height: 40px;" />
          <div class="ms-2">
            <p class="text-muted mb-0" style="font-size: 0.6rem;">{{ message.sender_time }}</p>
            <div class="p-2 rounded" :class="{ 'bg-info text-black': message.isSender, 'bg-light': !message.isSender }" style="max-width: 100%;">
              <img v-if="message.img" :src="message.img" alt="Message Image"/>
              <span v-else>{{ message.text }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="input-group">
      <button class="btn"><i class="bi bi-emoji-smile"></i></button>
      <input type="text" placeholder="Type a Message" class="form-control" style="border: none;" />
      <button class="btn"><i class="bi bi-image"></i></button>
      <button class="btn"><i class="bi bi-paperclip"></i></button>
      <button class="btn"><i class="bi bi-mic"></i></button>
    </div>

    <div v-if="showBlock" class="popup-overlay" @click.self="showBlock = false">
      <div class="popup-content">
        <i class="bi bi-slash-circle" style="font-size: 24px; color: #6f42c1;"></i>
        <p style="color: #333; margin: 10px 0;">Block User</p>
        <p style="color: #666; font-size: 0.9rem; margin-bottom: 20px;">You are going to Block this User, Are you Sure?</p>
        <div style="display: flex; justify-content: space-between;">
          <button class="popup-btn cancel" @click="showBlock = false">Cancel</button>
          <button class="popup-btn confirm" @click="blockUser">Yes</button>
        </div>
      </div>
    </div>

    <div v-if="showDelete" class="popup-overlay" @click.self="showDelete = false">
      <div class="popup-content">
        <i class="bi bi-trash" style="font-size: 24px; color: #6f42c1;"></i>
        <p style="color: #333; margin: 10px 0;">Delete Conversation</p>
        <p style="color: #666; font-size: 0.9rem; margin-bottom: 20px;">Once you Delete this Conversation, You will not be able to undo this action</p>
        <div style="display: flex; justify-content: space-between;">
          <button class="popup-btn cancel" @click="showDelete = false">Cancel</button>
          <button class="popup-btn confirm" @click="deleteConversation">Yes</button>
        </div>
      </div>
    </div>

    <div v-if="showListsPopup" class="popup-overlay" @click.self="showListsPopup = false">
      <div class="popup-content">
        <i class="bi bi-unlock" style="font-size: 24px; color: #6f42c1;"></i>
        <p style="color: #333; margin: 10px 0;">Unlock User</p>
        <p style="color: #666; font-size: 0.9rem; margin-bottom: 20px;">You are going to unblock this User, Are you Sure?</p>
        <div style="display: flex; justify-content: space-between;">
          <button class="popup-btn cancel" @click="showListsPopup = false">Cancel</button>
          <button class="popup-btn confirm" @click="viewLists">Yes</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ChatConversation',
  data() {
    return {
      messages: [
        { id: 1, sender: "Andrew", text: "If I don’t like something, I’ll stay away from it.", sender_time: "Andrew, 2 hours ago", avatar: "/person4.1.jpg", isSender: false },
        { id: 2, sender: "Mathew Anderson", text: "If I don’t like something, I’ll stay away from it.", sender_time: "2 hours ago", avatar: "/person1.1.jpg", isSender: true },
        { id: 3, sender: "Andrew", text: "I want more detailed information.", sender_time: "Andrew, 2 hours ago", avatar: "/person4.1.jpg", isSender: false },
        { id: 4, sender: "Mathew Anderson", text: "If I don’t like something, I’ll stay away from it.", sender_time: "2 hours ago", avatar: "/person1.1.jpg", isSender: true },
        { id: 5, sender: "Mathew Anderson", text: "They got there early, and they really got good seats.", sender_time: "2 hours ago", avatar: "/person1.1.jpg", isSender: true },
        { id: 6, sender: "Andrew", img: '/image101.jpg', sender_time: 'Andrew, 2 hours ago', avatar: "/person4.1.jpg", isSender: false },
      ],
      showBlock: false,
      showDelete: false,
      showListsPopup: false,
    };
  },
  methods: {
    deleteConversation() {
      alert('Conversation deleted!');
      this.showDelete = false;
    },
    blockUser() {
      alert('User blocked!');
      this.showBlock = false;
    },
    viewLists() {
      alert('Viewing chat lists!');
      this.showListsPopup = false;
    },
  },
};
</script>

<style scoped>
.chatconversation {
  border-radius: 10px;
}

.chat-container {
  background-color: #fff;
  padding: 10px;
  border-bottom: 1px solid #e9ecef;
}

.bg-primary {
  background-color: #6f42c1 !important;
}

.text-lg {
  font-size: 1rem;
}

.fw-bold {
  font-weight: 700;
}

.btn-sm img {
  vertical-align: middle;
  height: 16px;
  width: 16px;
}

.popup-overlay {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}

.popup-content {
  background-color: #ffffff;
  padding: 20px;
  border-radius: 8px;
  width: 300px;
  text-align: center;
}

.popup-btn {
  padding: 8px 16px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  font-size: 0.9rem;
  margin: 0 5px;
}

.cancel {
  background-color: #858484;
  color: #fff;
}

.confirm {
  background-color: #6f42c1;
  color: #fff;
}

</style>