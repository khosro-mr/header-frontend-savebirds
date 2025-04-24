<template>
  <header class="app-header py-2 bg-white shadow-sm">
    <div class="container">
      <nav class="navbar navbar-expand-lg navbar-light">
        <!-- Left Section: Logo and Site Name -->
        <router-link to="/" class="navbar-brand d-flex align-items-center">
          <img src="/images/logo.png" alt="SaveBirds Logo" class="logo me-2" height="40">
          <span class="site-name fw-bold">SaveBirds</span>
        </router-link>

        <!-- Hamburger Menu for Mobile -->
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" 
                data-bs-target="#navbarContent" aria-controls="navbarContent" 
                aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>

        <!-- Center Section: Navigation Menu -->
        <div class="collapse navbar-collapse" id="navbarContent">
          <ul class="navbar-nav mx-auto">
            <li class="nav-item">
              <router-link to="/" class="nav-link" active-class="active">Home</router-link>
            </li>
            <li class="nav-item">
              <router-link to="/metrics" class="nav-link" active-class="active">Metrics</router-link>
            </li>
            <li class="nav-item">
              <router-link to="/presence-absence" class="nav-link" active-class="active">Presence-Absence Data</router-link>
            </li>
            <li class="nav-item">
              <router-link to="/bird-atlas" class="nav-link" active-class="active">Bird Atlas Generator</router-link>
            </li>
            <li class="nav-item">
              <router-link to="/team" class="nav-link" active-class="active">Our Team</router-link>
            </li>
            <li class="nav-item">
              <router-link to="/projects" class="nav-link" active-class="active">Ongoing Projects</router-link>
            </li>
          </ul>

          <!-- Right Section: Action Button -->
          <div class="d-flex">
            <router-link to="/metrics" class="btn btn-success rounded-pill px-4">
              Get Started
            </router-link>
          </div>
        </div>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: 'AppHeader'
}
</script>

<style scoped>
.active {
  font-weight: bold;
  text-decoration: underline;
}

.logo {
  max-height: 40px;
  width: auto;
}

.site-name {
  font-size: 1.2rem;
}

.nav-link {
  margin: 0 0.5rem;
  position: relative;
}

.nav-link:hover {
  color: #28a745;
}

@media (max-width: 992px) {
  .navbar-nav {
    margin-top: 1rem;
    margin-bottom: 1rem;
  }
  
  .d-flex {
    margin-top: 0.5rem;
    justify-content: center;
  }
}
</style> 