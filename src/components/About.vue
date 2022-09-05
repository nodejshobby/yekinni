<template>
  <section class="container section-padding" id="about">
    <div class="row text-center section-header">
        <div class="col-12">
            <h2>About Me</h2>
            <p>I like doing the most in both self-managed and team-based projects.</p>
        </div>
    </div>
    <div class="row mt-3 justify-content-center align-items-center g-3">
        <div class="col-md-6 text-center mb-4 mb-lg-0 d-flex align-items-center justify-content-center" data-aos="flip-down">
            <img class="img-fluid" src="../assets/rsz_2nodejshobby.png" id="about-me-image" alt="">
        </div>
        <div class="col-11 col-md-6 about-text" data-aos="flip-down">
            <h2 class="mb-3">Who I am</h2>
           <p> I am a passionate and result-driven <b>fullstack web developer</b> with 3 years hands-on experience using Php, JavaScript and its related stacks in building secure and scalable web applications. I am extremely skillful using Relational Databases such as MySQL and PostgreSQL, and No SQL databases like MongoDB. I am productive in both team-based and self-managed projects.</p>
           <a href="https://drive.google.com/file/d/1Vd_A8Ma6n4gzxGEPlZQmP7UVbbiib0pG/view" class="btn btn-outline-dark blue-hover-effect mt-2 p-2 px-3" target="_blank"><i class="fa fa-download"></i> Download my CV</a>
        </div>
    </div>
  </section>
</template>

<script>
export default {
    name: 'AboutSection'
}
</script>

<style>
    #about-me-image {
        vertical-align: middle;
        border-radius: 10%;
    }
    .section-header h2{
        font-size: 2.2rem;
        font-weight: 600;
    }
    .about-text p {
        line-height: 1.8;
    }
</style>