<template>
    <section class="container-fluid section-padding" id="project">
    <div class="row text-center section-header">
        <div class="col-12">
            <h2>Projects</h2>
            <p>Here are my projects with live demo</p>
        </div>
    </div>
    <div class="container">
        <div class="row justify-content-center g-4 mt-3">
            <div class="col-md-6 col-lg-4 shadow-sm" v-for="project in projects" :key="project.projectTitle">
                <div class="card bg-white project h-100">
                    <img class="card-img-top img-fluid" :src="project.projectImage" alt="">
                    <div class="card-body">
                        <div class="tags mt-1 mb-3"><span v-for="tag in project.projectTags" :key="tag">{{ tag }}</span></div>
                        <div class="d-flex justify-content-between align-items-center mb-3">
                            <h4>{{ project.projectTitle }}</h4>
                            <a target="_blank" :href="project.projectDemo" class="btn btn-sm btn-outline-primary demo"><i class="fas fa-link"></i></a>
                        </div>
                        
                        <p class="mb-4">{{ project.projectDescription }}</p>
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
        overflow: hidden;
        padding-bottom: .4rem;
    }
    .project p {
        font-size: .9rem;
    }
    .project h4 {
        font-size: 1.7rem;
    }
    .project .card-img-top {
        height: 11rem !important;
        border-bottom: .1px solid #e6e6e6;
        transition: transform .5s ease;
    }
    .project .card-img-top:hover {
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
        color: var(--primary-color);
        padding: .4rem .6rem;
        font-weight: 600;
        font-size: 17px;
        transition: all .5s ease;
    }
    .demo:hover, .demo:focus {
        background-color: var(--primary-color) !important;
        border: none;
    }
</style>