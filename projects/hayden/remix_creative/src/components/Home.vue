<template>
    <div class="home">
        <div class="banner">
            <img src="../assets/home-banner.png" alt="">
            <h1>This is <br>Remix Creative</h1>
        </div>
        <!-- / banner -->

        <div class="holder">
            <div class="projects">
                <ul>
                    <li></li>
                </ul>
            </div>
            <!-- / projects -->
        </div><!-- / holder -->
    </div>
    <!-- / home -->
</template>

<script>
export default {
    name: 'home',
    data() {
        return {
            msg: 'Welcome to Your Vue.js App',
            projects: [],
            projectCovers: []
        }
    },
    methods: {
        getProjects: function() {
            this.$http.jsonp('http://behance.net/v2/users/mattharvey/projects?api_key=wmkhz92FaRjQt4LZzE0L3akK6CXqQOMB')
            .then(response => {
                this.projects = response.body.projects;
                var shuffle = require('shuffle-array')
                shuffle(this.projects)
                console.log(JSON.parse(JSON.stringify(this.projects)))
            });
        }
    },
    created: function() {
        this.getProjects();
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

ul {
    list-style-type: none;
    padding: 0;
}

li {
    display: inline-block;
    margin: 0 10px;
}

.banner {
    position: relative;
}

.banner img {
    opacity: 0.7;
}

.banner h1 {
    position: absolute;
    top: 30%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: 140px;
    text-transform: uppercase;
    font-weight: 800;
    width: 80%;
}

</style>
