<template>
   <div class="card">
                <div class="card-header">Cuentame un nuevo chiste</div>
     
                <div class="card-body">
                       <form action="" v-on:submit.prevent="nuevochiste()">
                             <div class="form-group">
                                 <label for="">Titulo</label>
                                 <input type="text" class="form-control" name="titulo" v-model="titulo">
                             </div>
                             <div class="form-group">
                                <label for="">Chiste</label>
                                <textarea name="chiste" id="" class="form-control" v-model="chiste"></textarea>
                            </div>
                            <button type="submit" class="btn btn-primary">Enviar Chiste</button>
                       </form>
                </div>
            </div>
</template>

<script>
    export default {
        data(){
          return {
              titulo: '',
              chiste:''
          }
        },
        mounted() {
            console.log('Component mounted.')
        },
        methods: {
            
            nuevochiste(){
                const chiste ={
                    titulo:this.titulo,
                    chiste:this.chiste
                }
                this.$emit('new',chiste);
                alert(this.titulo);
            }

        },
    }
</script>
