<template>
    <header class="header">
      <div class="header-left">
        <img src="/image1.png" alt="HiTeam Logo" class="logo" />
        <span class="app-title">Hi TEAM</span>
      </div>
  
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
  .header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background-color: white;
    padding: 12px 20px;
    border-bottom: 1px solid #ddd;
    height: 60px; 
    width: 100%;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 1000;
  }
  
  .header-left {
    display: flex;
    align-items: center;
  }
  
  .logo {
    height: 40px; 
    margin-right: 10px;
  }
  
  .app-title {
    font-size: 20px;
    font-weight: bold;
    color: #333;
  }
  
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
  