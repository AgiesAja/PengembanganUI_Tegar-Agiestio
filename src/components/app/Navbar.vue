<template>
  <nav class="navbar">
    <div class="nav-brand">
      <router-link to="/">Gatherly</router-link>
    </div>
    <ul class="nav-links">
      <li><router-link to="/">Home</router-link></li>
      <li><router-link to="/about">About</router-link></li>
      <li><router-link to="/browse">Browse</router-link></li>
      <li><router-link to="/contact">Contact</router-link></li>
    </ul>
  </nav>
</template>

<style scoped>
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1.2rem 2rem;
  background: white;
  border-bottom: 1px solid #f0f0f0;
  margin-bottom: 2rem;
}
.nav-brand a {
  font-size: 1.5rem;
  font-weight: 800;
  color: #1c1948;
  text-decoration: none;
}
.nav-links {
  display: flex;
  gap: 2rem;
  list-style: none;
}
.nav-links a {
  text-decoration: none;
  color: #555;
  font-weight: 500;
  transition: color 0.2s;
}
.nav-links a:hover,
.nav-links .router-link-exact-active {
  color: #6644ff;
}
</style>

<style scoped>
/* NAVBAR FULL-WIDTH menyatu dengan bagian atas layar */
.navbar {
  width: 100%;
  background: var(--nav-bg, #1c1948);
  border-bottom: 1px solid var(--nav-border, #333);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.15);
  position: sticky;
  top: 0;
  z-index: 999;
  transition: all 0.3s cubic-bezier(0.16, 1, 0.3, 1);
}

.navbar-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  max-width: 1440px;
  margin: 0 auto;
  padding: 0.85rem 2rem;
}

/* Lampiran CSS */
.navbar.scrolled {
  background: rgba(28, 25, 72, 0.9);
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
}

.logo {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  text-decoration: none;
  color: var(--text-white, #fff);
  padding-right: 2rem;
  transition: transform 0.3s ease;
}

.logo:hover {
  transform: translateY(-2px);
}

.logo-icon {
  transition: transform 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
}

.logo:hover .logo-icon {
  transform: rotate(15deg) scale(1.1);
}

.logo-text {
  font-size: 1.15rem;
  font-weight: 700;
  letter-spacing: -0.01em;
}

.nav-menu {
  display: flex;
  align-items: center;
  gap: 2.5rem;
  list-style: none;
  margin: 0;
  padding: 0;
  flex: 1;
  justify-content: center;
}

.nav-item {
  position: relative;
  display: flex;
  align-items: center;
  height: 100%;
  padding: 1rem 0;
}

.nav-link {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  text-decoration: none;
  color: var(--text-white, #fff);
  font-size: 0.95rem;
  font-weight: 500;
  padding: 0.5rem 1.25rem;
  border-radius: 10px;
  transition: all 0.3s ease;
}

.nav-link.active {
  background-color: var(--primary, #6644ff);
  font-weight: 600;
  box-shadow: 0 4px 15px rgba(102, 68, 255, 0.3);
}

.nav-link.active:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(102, 68, 255, 0.5);
}

.nav-link:not(.active):hover {
  background-color: rgba(255, 255, 255, 0.1);
  transform: translateY(-2px);
}

.dropdown-indicator {
  transition: transform 0.3s ease;
}

.nav-item:hover .dropdown-indicator {
  transform: rotate(180deg);
}

/* ==================================
   DROPDOWN & SUBMENU STYLES
   Inspired by user reference image
   ================================== */

.dropdown-menu {
  display: none;
  position: absolute;
  top: 100%;
  left: 0;
  background-color: #d8d8d8;
  min-width: 200px;
  list-style: none;
  padding: 0;
  margin: 0;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
  border-radius: 4px;
}

/* Tampilkan dropdown level 1 saat nav-item di-hover */
.nav-item:hover .dropdown-menu {
  display: block;
  animation: fadeIn 0.2s ease-out;
}

.dropdown-item {
  position: relative;
}

.dropdown-link {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 12px 20px;
  text-decoration: none;
  color: #333;
  font-size: 0.95rem;
  transition:
    background-color 0.2s,
    color 0.2s;
  border-bottom: 1px solid rgba(0, 0, 0, 0.05);
}

.dropdown-link:hover {
  background-color: #c4c4c4;
  color: #000;
}

/* Hilangkan border bawah pada item terakhir */
.dropdown-item:last-child .dropdown-link {
  border-bottom: none;
}

/* Submenu (Level 2) */
.submenu {
  display: none;
  position: absolute;
  top: 0;
  left: 100%;
  background-color: #d8d8d8;
  min-width: 220px;
  list-style: none;
  padding: 0;
  margin: 0;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
  border-radius: 4px;
}

/* Tampilkan submenu level 2 saat dropdown-item di-hover */
.dropdown-item:hover .submenu {
  display: block;
  animation: fadeIn 0.2s ease-out;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(-5px);
  }

  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ==================================
   RIGHT SECTION
   ================================== */

.nav-right {
  display: flex;
  align-items: center;
  gap: 1.5rem;
}

.lang-selector {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  color: var(--text-white, #fff);
  font-size: 0.9rem;
  font-weight: 600;
  cursor: pointer;
  padding: 0.5rem;
  border-radius: 8px;
  transition: all 0.3s ease;
}

.lang-selector:hover {
  background: rgba(255, 255, 255, 0.1);
}

.lang-selector:hover .chevron {
  transform: translateY(2px);
}

.chevron {
  transition: transform 0.3s ease;
  margin-top: 2px;
}

.hamburger-btn {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 44px;
  height: 44px;
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.05);
  border-radius: 10px;
  color: var(--text-white, #fff);
  cursor: pointer;
  transition: all 0.3s cubic-bezier(0.34, 1.56, 0.64, 1);
}

.hamburger-btn:hover {
  background: rgba(255, 255, 255, 0.15);
  transform: scale(1.05);
}

@media (max-width: 900px) {
  .nav-menu {
    gap: 1rem;
  }
}

@media (max-width: 768px) {
  .nav-menu {
    display: none;
  }

  .lang-selector {
    display: none;
  }
}
</style>
