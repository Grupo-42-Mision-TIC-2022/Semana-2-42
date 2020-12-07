<template>
    
    <div id="team" class="card text-white bg-dark">
        <div class="d-flex justify-content-center p-2">
           <img v-bind:src="member.image" alt="Fotografía del equipo">
        </div>
        <div class="card-body">
            <h3 class="card-title">{{member.nombre}}</h3>
            <p class="card-text">{{member.descripcion}}</p>
        </div>
        <div class="card-footer">
            <h6 class="text-muted"><span> Rol:</span>{{member.rol}}</h6>
            <small class="text-muted"><span>  Código:</span>{{member.codigo}}</small>
        </div>
    </div>
                    
</template>

<script>
    export default {
        name: "TeamCard",
        props: ['member']
    }
</script>

<style scoped>

</style>
