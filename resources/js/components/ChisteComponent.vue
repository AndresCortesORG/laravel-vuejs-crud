<template>
     <div class="card">
                <div class="card-header">{{ chiste.titulo}}</div>

                <div class="card-body">
                     <p>{{  chiste.chiste }}</p>
                </div>
                <div class="card-footer">
                    <button class="btn btn-info btn-sm text-white">Editar</button>
                    <button class="btn btn-danger btn-sm">Eliminar</button>
                </div>
            </div>
</template>

<script>
    export default {
        props:['chiste'],

        data(){
           return {
             
           };
        },
        mounted() {
            console.log('Component mounted.')
        }
    }
</script>
