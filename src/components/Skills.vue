<template>
   <section class="container-fluid section-padding" id="skill">
    <div class="row text-center section-header">
        <div class="col-12">
            <h2>Skills</h2>
            <p>Here are programming languages , databases and tools I use</p>
        </div>
    </div>
    
        <div class="row justify-content-center align-items-center g-5 px-3 px-md-5 mt-1" id="skill-box">
                <div class="col-md-6">
                    <h4 class="mb-4">Programming Languages</h4>
                    <SkillBar :width="90" title="HTML" color="#04AA6D" />
                    <SkillBar :width="80" title="CSS" color="#2196F3" />
                    <SkillBar :width="90" title="JAVASCRIPT" color="#f80000" />
                    <SkillBar :width="80" title="PHP" color="#000328" />
                    <SkillBar :width="90" title="NODEJS" color="#808080" />
                </div>
                <div class="col-md-6">
                    <h4 class="mb-4">Tools and Databases</h4>
                    <SkillBar :width="90" title="MONGODB" color="#04AA6D" />
                    <SkillBar :width="80" title="MYSQL" color="#2196F3" />
                    <SkillBar :width="90" title="REDIS" color="#f80000" />
                    <SkillBar :width="80" title="GIT" color="#000328" />
                    <SkillBar :width="90" title="HEROKU,NETLIFY & AWS" color="#808080" />
                </div>
        </div>  
    </section>
</template>

<script>
import SkillBar from './SkillBar.vue';

export default {
    name: "SkillSection",
    components: {
        SkillBar,
    }
}
</script>