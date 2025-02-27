<template>
    <div class="body-container">
        <div class="button-container">
            <h2 class="about-button" @click="show = !show">{{show ? "Hide" : "About Me"}}</h2>
        </div>
        <Transition>
            <div v-if="show" class="about-me">
                <p>
                    Hi, I’m Will Barnard. I’m a Software Developer with a passion for collaborating with others and building meaningful programs. 
                    I am a fast learner and self-starter with a proven history working on a team.
                </p>
                <p>
                    I found my passion for working in technology in my most recent role animating sheet music for the startup technology company Trala. 
                    Working at a small tech company of about 20 people gave me the opportunity to work closely with software developers and acquire technology skill on the job, 
                    and I even found opportunities to apply time-saving code scripting in my creative workflows. 
                    This passion I found for technology led me to enroll at Tech Elevator, an intense 14-week full stack software development course.
                </p>
                <p>
                    Having completed the program with Tech Elevator, I am now looking for a role as a software developer. 
                    While I continue to make software-based solutions for Trala, I have built a portfolio of full stack web applications and am currently deploying them to my home server using Docker and Nginx. 
                    Projects include Train Tracker: a web interface for tracking Chicago trains and viewing data analytics I have generated about prediction accuracy, 
                    Virtual Vibes: a post and message forum, and Kitchen Jam: a web app for logging meals you cook and becoming a better chef.
                </p>
            </div>
        </Transition>
    </div>
    
</template>

<script>
export default {
    data() {
        return {
            show: false
        }
    }
}
</script>

<style>
    .body-container {
        width: 100%
    }
    .about-button {
        color: #00bd7e;
        border: 2px solid;
        border-radius: 10px;
        padding: 10px 20px;
        margin: 0px;
        margin-bottom: 10px;
        cursor: pointer;
        width: auto;
    }
    .show-button {
        border-radius: 10px;
        margin: 0px;
        padding: 0px;
        width: 100%;
    }
    .about-button:hover {
        color: #00bd7e33;
    }
    .about-me p {
        margin-bottom: 10px;
        text-align: left;
    }
    .button-container {
        display: flex;
        justify-content: center;
    }
</style>