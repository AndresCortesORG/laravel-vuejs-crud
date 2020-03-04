

    <template>             
    <div class="row justify-content-center">
        <div class="col-md-4">
            <form-chiste-component @new="agregarChiste"></form-chiste-component>
        </div>
        <div class="col-md-8">
            <chiste-component  v-for="chiste in chistes" :key="chiste.id"  :chiste="chiste"></chiste-component>
        </div>
    </div>
    </template>

<script>
    export default {
        data(){
            return {
                chistes: [{
                    titulo: 'Chiste malo',
                    chiste:'sergio tiene cara de oscaar'
                }]
            }
        },
        mounted() {
            console.log('Component mounted.')
        },methods: {
            agregarChiste(chiste){
              this.chistes.push(chiste);
            }
        },
    }
</script>
