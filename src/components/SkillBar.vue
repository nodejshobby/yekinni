<template>
    <div class="mb-4">
        <h6 class="skill-title">{{ title }}</h6>
        <div class="container-skill">
            <div class="skills" :style="{ 'width': `${width}%`, 'background-color': color}">{{ `${width}%` }}</div>
        </div>
    </div>
    
</template>

<script>
export default {
    name: 'SkillBar',
    props: {
        title: String,
        width: Number,
        color: String
    }
}
</script>

<style>
    .container-skill {
        width: 100%; 
        background-color: #ddd;
        border-radius: .4rem;
    }

    .skill-title {
        color: var(--primary-color);
        margin-bottom: .7rem;
        font-size: .9rem;
    }
    .skills {
        text-align: right; 
        padding: 1px 0; 
        color: var(--secondary-color);
        border-radius: .4rem;
    }
</style>