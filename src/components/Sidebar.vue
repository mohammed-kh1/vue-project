<template>
  <nav class="col-12 col-md-2 bg-light p-3 border-end" style="background-color: #f7f7f7; margin: 0; padding-left: 0;">
    <ul class="list-unstyled">
      <li class="mb-2">
        <button class="btn btn-primary w-100 d-flex align-items-center justify-content-start text-start py-2" style="background-color: #6f42c1; border-color: #6f42c1;">
          <i class="bi bi-speedometer2 me-2"></i> Dashboard
        </button>
      </li>
      <li class="mb-2">
        <button class="btn btn-outline-secondary w-100 d-flex align-items-center justify-content-start text-start py-2">
          <i class="bi bi-cart me-2"></i> Orders
        </button>
      </li>
      <li class="mb-2">
        <button class="btn btn-outline-secondary w-100 d-flex align-items-center justify-content-start text-start py-2">
          <i class="bi bi-people me-2"></i> Passengers
        </button>
      </li>
      <li class="mb-2">
        <button class="btn btn-outline-secondary w-100 d-flex align-items-center justify-content-start text-start py-2">
          <i class="bi bi-person-gear me-2"></i> Captains
        </button>
      </li>
      <li class="mb-2">
        <button class="btn btn-outline-secondary w-100 d-flex align-items-center justify-content-start text-start py-2">
          <i class="bi bi-list-ul me-2"></i> Categories
        </button>
      </li>
      <li class="mb-2">
        <button class="btn btn-outline-secondary w-100 d-flex align-items-center justify-content-start text-start py-2">
          <i class="bi bi-cash-coin me-2"></i> Settlement
        </button>
      </li>
      <li class="mb-2">
        <button class="btn btn-outline-secondary w-100 d-flex align-items-center justify-content-start text-start py-2">
          <i class="bi bi-envelope me-2"></i> Contact
        </button>
      </li>
      <li class="mb-2">
        <button class="btn btn-outline-secondary w-100 d-flex align-items-center justify-content-start text-start py-2">
          <i class="bi bi-star me-2"></i> Reviews
        </button>
      </li>
      <li class="mb-2">
        <button class="btn btn-outline-secondary w-100 d-flex align-items-center justify-content-start text-start py-2">
          <i class="bi bi-shield-lock me-2"></i> Permissions
          <select class="form-select ms-2" style="width: auto; display: inline; padding: 2px 8px; font-size: 0.875rem;">
            <option value="all">All</option>
            <option value="admin">Admin</option>
            <option value="user">User</option>
          </select>
        </button>
      </li>
      <li class="mb-2">
        <button class="btn btn-outline-secondary w-100 d-flex align-items-center justify-content-start text-start py-2">
          <i class="bi bi-translate me-2"></i> Translation
        </button>
      </li>
      <li class="mb-2">
        <button class="btn btn-outline-secondary w-100 d-flex align-items-center justify-content-start text-start py-2">
          <i class="bi bi-camera-video me-2"></i> Education Video
        </button>
      </li>
      <li class="mb-2">
        <button class="btn btn-outline-secondary w-100 d-flex align-items-center justify-content-start text-start py-2">
          <i class="bi bi-gear me-2"></i> Settings
        </button>
      </li>
      <li class="mb-2">
        <button class="btn btn-outline-secondary w-100 d-flex align-items-center justify-content-start text-start py-2">
          <i class="bi bi-file-text me-2"></i> Content
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

<style scoped>
.btn-primary {
  color: #fff !important;
}

.btn-outline-secondary {
  color: #6c757d !important;
  border-color: #ced4da !important;
}

.btn-outline-secondary:hover {
  background-color: #6f42c1 !important;
  color: #fff !important;
  border-color: #6c757d !important;
}

.form-select {
  background-color: #fff;
  border-color: #ced4da;
  border-radius: 0.25rem;
  height: 28px; 
  font-size: 0.875rem;
  color: #6c757d;
}

.btn-outline-secondary .form-select {
  margin-left: 8px;
  vertical-align: middle;
}
</style>