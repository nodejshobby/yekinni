<template>
  <nav class="navbar navbar-expand-md navbar-dark bg-dark fixed-top shadow-sm px-1 px-md-3" id="scrollNavbar">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Yekinni <b style="color: var(--light-blue);">B.</b></a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarScroll" aria-controls="navbarScroll" aria-expanded="false" aria-label="Toggle navigation">
      <i class="fa fa-bars"></i>
    </button>
    <div class="collapse navbar-collapse" id="navbarScroll">
      <ul class="navbar-nav ms-auto my-2 my-lg-0">
        <li class="nav-item">
          <a class="nav-link" aria-current="page" href="#hero-section">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#about">About</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#project">Projects</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#skill">Skills</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#contact">Contact</a>
        </li>
      </ul>
      <div class="d-flex ms-md-4 me-md-2 mb-2 mb-lg-0">
        <a href="https://api.whatsapp.com/send?phone=2348132961732&text=Hello%2C%20Yekinni%20Basiru" target="_blank" class="btn btn-primary btn-action">Hire me</a>
        </div>
    </div>
    
  </div>
</nav>
</template>

<script>
export default {
    name: "NavBar"
}
</script>

<style>
    .navbar {
        background-color: var(--primary-color) !important;
    }
    .navbar-brand {
        font-size: 1.6rem;
        font-weight: 600;   
    }
    .navbar-toggler {
        font-size: 1.7rem;
        color: var(--secondary-color);
        border: none;
    }
    .navbar-toggler:focus {
        outline: none !important;
        border: none !important;
        box-shadow: none !important;
    }
    .nav-link {
        color: var(--secondary-color) !important;
        transition: all 0.5s ease;
    }

    .nav-link:hover  {
        color: var(--light-blue) !important;
    }
    
    .nav-link.active {
      color: var(--light-blue) !important;
      font-weight: 600;
    }

    .nav-link:active {
      color: var(--light-blue) !important;
      font-weight: 600;
    }
    
    
    
</style>