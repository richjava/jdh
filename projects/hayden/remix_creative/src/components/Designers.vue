<template>
    <div class="our-people">
        <div class="banner">
            <img src="../assets/home-banner.png" alt="">
            <h1>This is <br>Remix Creative</h1>
        </div>
        <!-- / banner -->

        <div class="designers">
            <h2>Here are our people</h2>
            <ul class="designer-list">
                <li class="designer" v-for="designer in designers">
                    
                </li>
            </ul>
        </div><!-- / designers -->
    </div><!-- / our people -->
</template>

<script>
export default {
    name: 'designers',
    data() {
        return {
            designers: []
            //users: ['mattharvey', 'vitorugo', 'rafaeldraws', 'stanleysun']
        }
    },
    methods: {
        getProjects: function() {
            this.$http.jsonp('http://behance.net/v2/users/haydenwrat86b8/projects?api_key=wmkhz92FaRjQt4LZzE0L3akK6CXqQOMB')
            .then(response => {
                this.designers = response.body.following;
            });
        },
    },
    created: function() {
        this.getProjects();
    }
}
</script>

<!-- styling for the component -->
<style>

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
    overflow: hidden;
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
