<template>
  <div class="breadcrumb-container">
    <ul class="breadcrumb">
      <li><router-link to="/">Home</router-link></li>
      <li v-if="$route.path !== '/'">{{ $route.meta.breadcrumb || $route.name }}</li>
    </ul>
  </div>
</template>

<style scoped>
.breadcrumb-container {
  margin-bottom: 2rem;
}
.breadcrumb {
  display: flex;
  list-style: none;
  gap: 0.5rem;
  color: #666;
  font-size: 0.95rem;
}
.breadcrumb li + li::before {
  content: "/";
  margin-right: 0.5rem;
  color: #ccc;
}
.breadcrumb a {
  color: #6644ff;
  text-decoration: none;
}
</style>

<style scoped>
.breadcrumb {
  margin-bottom: 2rem;
  padding: 1rem;
  background: rgba(255, 255, 255, 0.05);
  border-radius: 8px;
}

.breadcrumb ul {
  list-style: none;
  display: flex;
  padding: 0;
  margin: 0;
  align-items: center;
  gap: 0.5rem;
}

.breadcrumb a {
  text-decoration: none;
  color: var(--primary, #6644ff);
  font-weight: 500;
}

.breadcrumb a:hover {
  text-decoration: underline;
}

.separator {
  color: #888;
  margin: 0 0.5rem;
}

.active-crumb {
  color: #333;
  font-weight: 600;
}

@media (prefers-color-scheme: dark) {
  .active-crumb {
    color: #ccc;
  }
}
</style>
