<script setup>
</script>

<template>
    <nav class="navbar navbar-expand-lg bg-light sticky-top">
        <div class="container-fluid">
          <a class="navbar-brand" href="#portfolio">PORTFOLIO</a>
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
        
          <div class="collapse navbar-collapse " id="navbarSupportedContent">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0 w-100 justify-content-end">
              <li class="nav-item">
                <a class="nav-link" aria-current="page" href="https://github.com/dinsorkot?tab=repositories">project</a>
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
}
</style>
