<template>
    <div class="col">
            <div v-if="member.codigo % 2 === 0" class="footer-widget card text-white bg-dark">
                <div class="d-flex justify-content-center p-2"> <img class="team-image__img"
                        v-bind:src="member.imagen" alt="Developer"></div>
                <div class="card-body">
                    <h5 class="card-title">{{member.nombre}}</h5>
                    <p class="card-text" v-html=member.descripcion></p>
                    <p class="card-text" v-html=member.rol></p>
                    <p class="card-text" v-html=member.codigo></p>
                </div>
                <div class="card-footer bg-white"> <small class="text-muted">Last updated 3 mins
                        ago</small>
                </div>
            </div>
            <div v-else class="footer-widget card text-white bg-danger">
                <div class="d-flex justify-content-center p-2"> <img class="team-image__img"
                        v-bind:src="member.imagen" alt="Developer"></div>
                <div class="card-body">
                    <h5 class="card-title">{{member.nombre}}</h5>
                    <p class="card-text" v-html=member.descripcion></p>
                    <p class="card-text" v-html=member.rol></p>
                    <p class="card-text" v-html=member.codigo></p>
                </div>
                <div class="card-footer bg-white"> <small class="text-muted">Last updated 3 mins
                        ago</small>
                </div>
            </div>
        </div>
</template>

<script>
    export default {
        name: "TeamCard",
        props: {member: Object }
    }
</script>

<style scoped>
.footer-widget {
    border: 1px solid #444;
    height: 100%;
    width: 100%;
}
</style>
