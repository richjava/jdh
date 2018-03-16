<template>
    <div class="modal">
        <div class="modal-container">
            <div class="project-container"></div>
            <div class="project-info-container"></div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'modal',
    props: ['projectID'],
    methods: {
        showModal: function() {
            alert('working')
        },
        getProjectData: function(projectID) {
            this.$http.jsonp('http://www.behance.net/v2/projects/' + projectID + '?api_key=H0kzBzX75cebcL11a23UE6feEiqAMiZH')
                .then(response => {
                    this.selectedProject = response.body.project;
                    console.log(this.selectedProject);
                });
        }
    },
    watch: {
        projectID: function(projectID) {
            $('.modal').css('display', 'block');
            this.getProjectData(projectID);
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
    font-weight: normal;
}

.modal {
    position: fixed;
    z-index: 9998;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.7);
    transition: opacity .3s ease;
    display: none;
}

.modal-container {
    padding-top: 150px;
    width: 80%;
    height: 750px;
    margin: auto;
}

.project-container {
    width: 60%;
    height: 100%;
    background-color: white;
    display: inline-block;
    vertical-align: top;
}

.project-info-container {
    width: 400px;
    height: 100%;
    background-color: white;
    display: inline-block;
    vertical-align: top;
}

.project-image {
    width: 100%;
}
</style>