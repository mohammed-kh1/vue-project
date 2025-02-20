<template>
    <div class="col-12 col-md-4 p-3 border-end" style="background-color: #fff;">
      <h2 class="text-lg fw-bold mb-4" style="color: #333;">Contacts</h2>
      <div class="mb-4">
        <input type="text" placeholder="Search contacts" class="form-control border" style="border-color: #ced4da;" />
      </div>
      <div class="space-y-4">
        <div v-for="chat in chats" :key="chat.id" class="d-flex align-items-center mb-3">
          <img :src="chat.avatar" alt="Avatar" class="rounded-circle" style="width: 40px; height: 40px;" />
          <div class="ms-2">
            <p class="mb-0 fw-bold" style="color: #333;">{{ chat.name }}</p>
            <p class="text-muted mb-0" style="font-size: 0.8rem;">{{ chat.role }}</p>
          </div>
          <span class="ms-auto text-muted" style="font-size: 0.7rem;">{{ chat.status }}</span>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ChatList',
    data() {
      return {
        chats: [
          { id: 1, name: "Mathew Anderson", role: "Me", avatar: "/person1.png", status: "Away" },
          { id: 2, name: "Michael Flintoff", role: "Yesterday was great..", avatar: "/person2.png", status: "15 minutes ago" },
          { id: 3, name: "Bianca Anderson", role: "Nice looking dress you...", avatar: "/person3.png", status: "30 minutes ago" },
          { id: 4, name: "Andrew Johnson", role: "sent a photo", avatar: "/person4.png", status: "2 hours ago" },
          { id: 5, name: "Mark Stokes", role: "Lorem Ispusm text sud..", avatar: "/person5.png", status: "5 days ago" },
          { id: 6, name: "Lauren Ipsum", role: "Lorem Ispusm text..", avatar: "/person6.png", status: "30 minutes ago" },
          { id: 3, name: "Bianca Anderson", role: "Nice looking dress you...", avatar: "/person3.png", status: "30 minutes ago" },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .text-lg {
    font-size: 1.25rem;
  }
  
  .fw-bold {
    font-weight: 700;
  }
  </style>