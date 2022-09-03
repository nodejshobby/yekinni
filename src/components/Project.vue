<template>
    <section class="container-fluid section-padding" id="project">
    <div class="row text-center section-header">
        <div class="col-12">
            <h2>Projects</h2>
            <p>Here are my projects with live demo</p>
        </div>
    </div>
    <div class="container">
        <div class="row justify-content-center d-flex align-items-stretch g-4 mt-3">
            <div class="col-md-6 col-lg-4 shadow-sm" v-for="project in projects" :key="project.projectTitle">
                <div class="card bg-white project h-100">
                    <img class="card-img-top img-fluid" :src="project.projectImage" alt="">
                    <div class="card-body d-flex flex-column">
                        <div class="tags mt-1 mb-3"><span v-for="tag in project.projectTags" :key="tag">{{ tag }}</span></div>
                        <h3>{{ project.projectTitle }}</h3>
                        <p class="mb-4">{{ project.projectDescription }}</p>
                        <div class="d-flex justify-content-end mt-2">
                            <a target="_blank" :href="project.projectDemo" class="btn btn-sm btn-outline-primary demo">Check it out <i class="fa fa-arrow-right"></i></a>
                        </div>
                    </div>
                </div>
            </div>
            
        </div>
    </div>
    
    </section>
</template>

<script>
import data from '../data/projects';

export default {
    name: 'ProjectSection',
    data() {
        return {
            projects: data,
        }
},
}
</script>

<style>
    #project {
        background-color: var(--primary-color);
        color: white;
        margin-top: 2rem;
    }
    .project {
        background-color: var(--secondary-color);
        color: var(--dark-blue);
        box-shadow: 0 1rem 3rem rgba(0,0,0,.175)!important;
        padding-bottom: .8rem;
        overflow: hidden;
    }
    .project p {
        font-size: .9rem;
    }
    .project h2 {
        font-size: 1.8rem;
    }
    .project .card-img-top {
        height: 15rem !important;
        border-bottom: .2px solid #dadada;
        transition: transform .5s ease;
    }
    .project:hover .card-img-top {
        transform: scale(1.1);
    }
    .tags {
        line-height: 1.9;
    }
    .tags span {
        background-color: var(--dark-blue);
        color: var(--secondary-color);
        margin-right: .3rem;
        padding: .3rem .9rem;
        font-size: .7rem;
        border-radius: 20px;
        font-weight: 600;
        white-space: nowrap;
    }
    .demo {
        border-color: var(--primary-color);
        color: var(--dark-blue);
        padding: .4rem .8rem;
        font-weight: 600;
    }
    .demo:hover, .demo:focus {
        background-color: var(--primary-color) !important;
        border: none;
    }
</style>