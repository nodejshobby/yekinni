<template>
  <header class="container-fluid">
    <div class="row justify-content-center align-items-center text-center" id="hero-section">
        <div class="col-md-8">
            <h1 class="mb-3 animate__animated animate__bounce">Hi, 👋I'm Yekinni Basiru</h1>
            <p class="animate__animated animate__shakeX">Programmer | Fullstack Web Developer | Website Designer</p>
            <p class="animate__animated animate__shakeX"> I build scalable and secure web applications. <br>
            I am active in self and team managed projects.
            </p>
            <div class="social-icons mt-4 animate__animated animate__shakeX">
                <a href="https://www.linkedin.com/in/nodejshobby/" target="_blank"><i class="fab fa-linkedin"></i></a>
                <a href="https://github.com/nodejshobby" target="_blank"><i class="fab fa-github"></i></a>
                <a href="mailto:nodejshobby@gmail.com?subject=Hello%2C%20Yekinni%20Basiru" target="_blank"><i class="fa fa-envelope-open"></i></a>
            </div>
            <div class="cta mt-4 animate__animated animate__pulse">
                <a href="#project" class="btn btn-outline-light"> <i class="fa fa-laptop"></i> See my works</a>
            </div>
        </div>
    </div>
  </header>
</template>

<script>
export default {
    name: 'HeroSection'
}
</script>

<style>
    #hero-section {
        background-color: var(--primary-color) !important;
        color: var(--secondary-color);
        padding: 4rem 0;
    }
    .social-icons a {
        color: var(--secondary-color);
    }
    .social-icons i {
        font-size: 1.6rem;
        margin-right: .8rem;
    }
    .cta {
        color: var(--secondary-color);
    }
</style>