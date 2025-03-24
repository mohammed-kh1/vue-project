<template>
  <div class="col-12 col-md-12">
    <div class="left row col-md-12">
      <nav aria-label="breadcrumb" class="breadcrumb-container d-flex justify-content-between align-items-center">
        <div class="col-auto">
          <ol class="breadcrumb mt-2">
            <li class="breadcrumb-item">Chat</li>
          </ol>
        </div>
        <div class="col-auto d-flex justify-content-end align-items-center">
          <button class="icon-btn me-2">
              <i class="bi bi-house-door"></i>
          </button>
          <span class="text-black me-2">/</span>
          <button class="icon-btn bs-dark-bg-subtle" style="background-color: #d6d6d6;">
              <span class="text-primary">Chat</span>
          </button>
      </div>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Breadcrumb'
};
</script>

<style scoped>
.breadcrumb-container {
  background-color: #ffffff;
  margin-top: 90px;
  margin-left: 42px;
  width: 97%;
  height: 50px;
  border-radius: 10px;
}

.breadcrumb-item{
  font-size: 1.2rem;
  font-weight: bold;
}

.icon-btn.bs-dark-bg-subtle {
border-radius: 10px; 
padding: 2px 8px; 
}

.icon-btn {
  background: none;
  border: none;
  color: #303030; 
}
</style>