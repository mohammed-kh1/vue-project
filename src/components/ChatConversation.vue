<template>
    <div class="col-12 col-md-8 p-3" style="background-color: #f8f9fa;">
      <div class="d-flex justify-content-between align-items-center mb-3">
        <h2 class="text-lg fw-bold mb-0" style="color: #333;">Chat</h2>
        <div>
          <button class="btn btn-outline-secondary btn-sm me-2" style="border-color: #ced4da; color: #6c757d;">
            <i class="bi bi-search"></i>
          </button>
          <button class="btn btn-outline-secondary btn-sm me-2" style="border-color: #ced4da; color: #6c757d;">
            <i class="bi bi-phone"></i>
          </button>
          <button class="btn btn-outline-secondary btn-sm" style="border-color: #ced4da; color: #6c757d;">
            <i class="bi bi-chat-dots"></i>
          </button>
        </div>
      </div>
      <div class="chat-container h-[calc(100vh-200px)] overflow-y-auto mb-3" style="max-height: calc(100vh - 200px); background-color: #fff; border-radius: 5px; border: 1px solid #e9ecef;">
        <div v-for="message in messages" :key="message.id" class="mb-3 p-2">
          <div class="d-flex align-items-start" :class="{ 'flex-row-reverse': message.isSender }">
            <img :src="message.avatar" alt="Avatar" class="rounded-circle" style="width: 32px; height: 32px;" />
            <div class="ms-2" :class="{ 'me-2': message.isSender }">
              <p class="mb-0 fw-bold" style="color: #333;">{{ message.sender }}</p>
              <div class="p-2 rounded" :class="{ 'bg-primary text-white': message.isSender, 'bg-light': !message.isSender }" style="max-width: 70%;">
                {{ message.text }}
              </div>
              <p class="text-muted mb-0" style="font-size: 0.7rem;">{{ message.time }}</p>
            </div>
          </div>
        </div>
      </div>
      <div class="input-group">
        <input type="text" placeholder="Type a Message" class="form-control border" style="border-color: #ced4da;" />
        <button class="btn btn-outline-secondary" style="border-color: #ced4da; color: #6c757d;">
          <i class="bi bi-send"></i>
        </button>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ChatConversation',
    data() {
      return {
        messages: [
          { id: 1, sender: "Mathew Anderson", text: "If I don’t like something, I’ll stay away from it.", time: "2 hours ago", avatar: "/person1.png", isSender: false },
          { id: 2, sender: "Andrew", text: "I want more detailed information.", time: "2 hours ago", avatar: "/person4.png", isSender: true },
          { id: 3, sender: "Mathew Anderson", text: "They got there early, and they really got good seats.", time: "2 hours ago", avatar: "/person1.png", isSender: false },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .chat-container {
    background-color: #fff;
    border-radius: 5px;
    padding: 10px;
    border: 1px solid #e9ecef;
  }
  
  .bg-primary {
    background-color: #6f42c1 !important;
  }
  
  .btn-outline-secondary {
    border-color: #ced4da !important;
    color: #6c757d !important;
  }
  
  .btn-outline-secondary:hover {
    background-color: #6c757d !important;
    color: #fff !important;
    border-color: #6c757d !important;
  }
  
  .text-lg {
    font-size: 1.25rem;
  }
  
  .fw-bold {
    font-weight: 700;
  }
  </style>