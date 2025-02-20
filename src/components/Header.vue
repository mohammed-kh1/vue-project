<template>
    <header class="header">
      <!-- Left Side: Logo & Title -->
      <div class="header-left">
        <img src="/image1.png" alt="HiTeam Logo" class="logo" />
        <span class="app-title">Hi TEAM</span>
      </div>
  
      <!-- Right Side: Icons & User Profile -->
      <div class="header-right">
        <button class="icon-btn">
          <i class="bi bi-bell"></i>
        </button>
        <button class="icon-btn">
          <i class="bi bi-moon"></i>
        </button>
        <button class="icon-btn">
          <i class="bi bi-globe"></i>
        </button>
        <div class="user-profile">
          <img src="/person1.png" alt="User Avatar" class="user-avatar" />
        </div>
      </div>
    </header>
  </template>
  
  <script>
  export default {
    name: "Header",
  };
  </script>
  
  <style scoped>
  /* Header Layout */
  .header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background-color: white;
    padding: 12px 20px;
    border-bottom: 1px solid #ddd;
    height: 60px; /* Consistent with sample */
    width: 100%;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 1000;
  }
  
  /* Left Side */
  .header-left {
    display: flex;
    align-items: center;
  }
  
  .logo {
    height: 40px; /* Adjust based on sample */
    margin-right: 10px;
  }
  
  .app-title {
    font-size: 20px;
    font-weight: bold;
    color: #333;
  }
  
  /* Right Side */
  .header-right {
    display: flex;
    align-items: center;
  }
  
  .icon-btn {
    background: none;
    border: none;
    font-size: 18px;
    margin-right: 15px;
    cursor: pointer;
    color: #555;
  }
  
  .icon-btn:hover {
    color: #000;
  }
  
  .user-profile {
    display: flex;
    align-items: center;
  }
  
  .user-avatar {
    height: 35px;
    width: 35px;
    border-radius: 50%;
  }
  </style>
  