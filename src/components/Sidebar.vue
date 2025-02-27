<template>
  <nav class="sidebar col-12 col-md-2" style="background-color: white;">
    <img src="/image1.png" alt="HiTeam Logo" class="logo" />
    <span class="app-title">Hi TEAM</span>
    <ul class="list-unstyled">
      <li class="mb-1 mt-4">
        <button class="btn btn-primary w-100 d-flex py-2" style="background-color: #6f42c1; border-color: #6f42c1;">
          <i class="bi-speedometer2 me-2"></i> Dashboard
        </button>
      </li>
      <li class="mb-1">
        <button class="btn w-100 d-flex py-2">
          <i class="bi-box me-2"></i> Orders
        </button>
      </li>
      <li class="mb-1">
        <button class="btn w-100 d-flex py-2">
          <i class="bi-people me-2"></i> Passengers
        </button>
      </li>
      <li class="mb-1">
        <button class="btn w-100 d-flex py-2">
          <i class="bi-truck me-2"></i> Captains
        </button>
      </li>
      <li class="mb-2 border-bottom">
        <button class="btn w-100 d-flex py-2">
          <i class="bi-clipboard-check me-2"></i> Categories
        </button>
      </li>
      <li class="mb-2 border-bottom">
        <button class="btn w-100 d-flex py-2">
          <i class="bi-card-text me-2"></i> Settlement
        </button>
      </li>
      <li class="mb-1">
        <button class="btn w-100 d-flex py-2">
          <i class="bi-envelope me-2"></i> Contact
        </button>
      </li>
      <li class="mb-2 border-bottom">
        <button class="btn w-100 d-flex py-2">
          <i class="bi-star me-2"></i> Reviews
        </button>
      </li>
      <li class="mb-1" style="display: inline-flex;">
        <button class="btn w-100 d-flex py-2">
          <i class="bi-shield-lock me-2"></i> Permissions
          <div class="dropdown ms-2">
            <button class="btn dropdown-toggle" type="button" id="userDropdown" data-bs-toggle="dropdown" style=" font-size: 0.9rem; margin-left: 50px;">
            </button>
          </div>
        </button>
      </li>
      <li class="mb-1">
        <button class="btn w-100 d-flex py-2">
          <i class="bi-translate me-2"></i> Translation
        </button>
      </li>
      <li class="mb-1">
        <button class="btn w-100 d-flex py-2">
          <i class="bi-camera-video me-2"></i> Education Video
        </button>
      </li>
      <li class="mb-1">
        <button class="btn w-100 d-flex py-2">
          <i class="bi-gear me-2"></i> Settings
        </button>
      </li>
      <li class="mb-1">
        <button class="btn w-100 d-flex py-2">
          <i class="bi-file-text me-2"></i> Content
        </button>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'Sidebar',
};
</script>

<style>
  
  .logo {
    height: 60px; 
    margin-left: 15px;
    margin-top: -5px;
  }
  
  .app-title {
    font-size: 12px;
    font-weight: 400;
    color: #333;
  }
</style>