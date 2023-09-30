<script setup>
</script>

<template>
  <nav class="navbar navbar-expand-lg bg-light sticky-top">
    <div class="container-fluid">
      <a class="navbar-brand" href="#portfolio">PORTFOLIO</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse " id="navbarSupportedContent">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0 w-100 justify-content-end">
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" id="navbarDarkDropdownMenuLink" role="button"
              data-bs-toggle="dropdown" aria-expanded="false">
              project
            </a>
            <ul class="dropdown-menu dropdown-menu-dark" aria-labelledby="navbarDarkDropdownMenuLink">
              <li><a class="dropdown-item" href="https://api-dota.netlify.app">API Project</a></li>
              <li><a class="dropdown-item" href="https://add-drop-mju.netlify.app">ADD-DROP Project</a></li>
              <li><a class="dropdown-item" href="https://card-like-unlike.netlify.app">Card Project</a></li>
              <li><a class="dropdown-item" href="https://from-mju.netlify.app">From Project</a></li>
              <li><a class="dropdown-item"
                  href="https://dinsorkot.github.io/corporate-ui-dashboard-main/pages/dashboard.html">DashBoard
                  Project</a></li>
              <li><a class="dropdown-item" href="dinsorkot.github.io/HTML01">WebProfile Project</a></li>
            </ul>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#contact">contact</a>
          </li>
        </ul>
      </div>

    </div>
  </nav>
</template>

<style scoped>
a {
  font-weight: 600;
}

span {
  height: 20px;
  width: 20px;
}

@media (max-width: 450px) {
  .gp btn {
    display: none;
  }
}</style>
