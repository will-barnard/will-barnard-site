<template>
    <div class="global">
        <h1>{{project.name}}</h1>
        <div class="image">
            <img :src="project.img" />
        </div>
        <h2>{{project.repo}}</h2>
        <div class="tags">
            <p v-for="tag in project.tags">&nbsp;#{{tag}}&nbsp;</p>
        </div>
        <h3>{{project.subtitle}}</h3>
        <div class="links">
            <div v-if="project.link">
                <a :href="project.link" target="_blank">🔗&nbsp;{{project.displayLink}}</a>
            </div>
            <div class="link-divider" v-if="project.link">
                <p>&nbsp;&nbsp;||&nbsp;&nbsp;</p>
            </div>
           
            <div>
                <a :href="project.githubUrl" target="_blank">🔗&nbsp;Github&nbsp;Repository</a>
            </div>
        </div>
        <Transition>
            <div v-show="showDetail">
                <p>{{project.description}}</p>
            </div>
        </Transition>
        <Transition>
            <div class="show" v-if="project.description">
                <h4 @click="showDetail = !showDetail">{{showDetail ? "Hide" : "Show"}} Description</h4>
            </div>
    </Transition>     
    </div>
</template>

<script>
export default {
    props: ['project'],
    data() {
        return {
            showDetail: false
        }
    },
    methods: {
        github() {
            
        }
    }
}
</script>

<style>
    h1 {
        text-align: center;
        font-size: 8vw;
    }
    .global {
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: start;
    }
    .image {
        width: 100%;
    }
    .image img {
        width: 100%;
        object-fit: contain;

    }
    .tags{
        display: flex;
        flex-wrap: wrap;
    }
    .tags p {
        border: 1px solid;
        border-radius: 15px;
        padding: 3px;
        margin-right: 5px;
        margin-bottom: 5px;
        background-color: var(--vt-c-indigo);
        color: var(--vt-c-white-soft);
    }
    .links {
        display: flex;
        justify-content: center;
    }
    .show {
        cursor: pointer;
        text-align: center;
    }
    .v-enter-active {
        transition: opacity 0.5s ease;
    }
    .v-enter-from {
        opacity: 0;
        transition: opacity 0.5s ease;
    }
    @media (min-width: 1024px) {
        h1 {
            font-size: 3vw;
        }
        .image img {
            width: 100%;
            object-fit: contain;
        }
    }
</style>