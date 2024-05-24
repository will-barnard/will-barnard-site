<template>
    <div>
        <div>
            <h2 class="about-button" @click="show = !show">{{show ? "Hide" : "About Me"}}</h2>
        </div>
        <Transform>
            <div v-show="show" class="about-me">
                <p>
                    Hi, I’m Will Barnard. I’m a Software Developer with a passion for collaborating with others and building meaningful programs. I am a fast learner and self-starter with a proven history working on a team.
                </p>
                <p>
                    I found my passion for working in technology in my most recent role animating sheet music for the music technology company Trala. Working at a small tech company of about 20 people gave me the opportunity to work closely with software developers and learn about the field, and I even found opportunities to apply time-saving code scripting in my creative workflows. This passion I found for technology led me to enroll at Tech Elevator, an intense 14-week full stack software development course.
                </p>
                <p>
                    Now, having completed the program with Tech Elevator, I am honing my skills and looking for a role as a software developer. I have built a portfolio of full stack web applications and am currently deploying them on my home server using Docker and Nginx. Projects include Train Tracker: a web interface for tracking Chicago trains and viewing data analytics I have generated about prediction accuracy, Virtual Vibes: a “Reddit” like message forum, and Kitchen Jam: a web app for logging meals you cook and becoming a better chef.
                </p>
            </div>
        </Transform>
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

<style scoped>
    .about-me {

    }
    .about-button {
        color: #00bd7e;
        border-radius: 10px;
        padding: 5px;
        cursor: pointer;
    }
    .about-button:hover {
        color: #00bd7e33;
    }
    p {
        margin-bottom: 10px;
    }
</style>