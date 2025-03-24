<template>
  <header class="header">
    <div class="header-left">
      <div>
        <button class="icon-btn">
          <i class="bi bi-search"></i>
        </button>
        <button class="icon-btn">
          <i class="bi bi-grid"></i>
        </button>
      </div>
    </div>
    <div class="header-right">
      <button class="icon-btn">
        <i class="bi bi-moon"></i>
      </button>
      <button class="icon-btn">
        <i class="bi bi-bell"></i>
      </button>
      <div class="dropdown language-dropdown me-2">
        <button class="btn dropdown-toggle" type="button" id="languageDropdown" data-bs-toggle="dropdown" aria-expanded="false">
          <img src="/ENG.png" alt="English language"/>
        </button>
        <ul class="dropdown-menu" aria-labelledby="languageDropdown">
          <li><a class="dropdown-item" href="#" >English</a></li>
          <li><a class="dropdown-item" href="#" >Arabic</a></li>
          <li><a class="dropdown-item" href="#" >Chinese</a></li>
        </ul>
      </div>
      <div class="user-profile">
        <img src="/person1.png" alt="User Avatar" class="user-avatar" />
      </div>
      <div class="dropdown ms-2">
        <button class="btn dropdown-toggle" type="button" id="userDropdown" data-bs-toggle="dropdown" style="padding: 1px 8px; font-size: 0.9rem; height: 35px;">
        </button>
        <ul class="dropdown-menu dropdown-menu-end" aria-labelledby="userDropdown">
          <li><a class="dropdown-item" href="#" >Profile</a></li>
          <li><a class="dropdown-item" href="#" >Sign Out</a></li>
          <li><a class="dropdown-item" href="#" >Settings</a></li>
          <li><a class="dropdown-item" href="#" >Help</a></li>
        </ul>
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

.form-select{
  font-size: 0.9rem;
}
.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: white;
  padding: 12px 20px;
  height: 55px; 
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
  margin-left: 222px;
  
}

.header-left {
  display: flex;
  align-items: center;
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
.btn img {
  margin-top: -4px;
  height: 18px;
  width: 20px;
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