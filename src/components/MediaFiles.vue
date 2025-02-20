<template>
    <aside class="col-12 col-md-2 bg-light p-3 border-start" style="background-color: #f7f7f7;">
      <h2 class="text-lg fw-bold mb-3" style="color: #333;">Media (36)</h2>
      <div class="row row-cols-2 g-2 mb-4">
        <div v-for="media in mediaItems" :key="media.id" class="col">
          <img :src="media.src" alt="Media" class="img-fluid rounded" style="height: 80px; object-fit: cover; border: 1px solid #e9ecef;" />
        </div>
      </div>
  
      <h2 class="text-lg fw-bold mb-3" style="color: #333;">Files (36)</h2>
      <ul class="list-unstyled">
        <li v-for="file in files" :key="file.id" class="d-flex align-items-center mb-2" style="font-size: 0.9rem; color: #6c757d;">
          <img :src="file.src" alt="File Icon" class="me-2" style="width: 30px; height: 30px; object-fit: cover; border-radius: 5px; border: 1px solid #ddd;" />
          <span>{{ file.name }} - {{ file.size }}</span>
        </li>
      </ul>
    </aside>
  </template>
  
  <script>
  export default {
    name: 'MediaFiles',
    data() {
      return {
        mediaItems: [
          { id: 1, src: "/media1.png" },
          { id: 2, src: "/media2.png" },
          { id: 3, src: "/media3.png" },
          { id: 4, src: "/media4.png" },
          { id: 1, src: "/media1.png" },
          { id: 2, src: "/media2.png" },
        ],
        files: [
          { id: 1, src: "/file1.png", name: "Service task.pdf", size: "1.5 MB" },
          { id: 2, src: "/file2.png", name: "Homepage design.fig", size: "2 MB" },
          { id: 3, src: "/file3.png", name: "About us.html", size: "2 MB" },
          { id: 4, src: "/file4.png", name: "Work project.zip", size: "3 MB" },
          { id: 5, src: "/file5.png", name: "Custom.js", size: "1 MB" },
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
  