<template>
    <div>

        <div v-for="call of storeCalls" v-bind:key="call.id" class="convocaria_conteiner conteiner-general " >
            <div class="wrapper ">

                     <div></div>
                        
                    <div class="convocaria "><strong>{{call.name}}</strong></div>

                    <div class="description padding-bottom ">
                        {{call.descriptions}}
                    </div>
                    
                    <div class="merito-section-conteiner  ">
                        <div class=" merito-conteiner_wrapper  ">

                            
                            <div class="merito-conteiner  ">
                                <div class="row padding-bottom  ">
                                    <!-- <div class="conteiner-general"> -->
                                        <div class="merito-number  "><strong>{{storeMerits[((call.id-1)*4)].name}}</strong></div>
                                        <div class="puntos-number  ">{{storeMerits[((call.id-1)*4)].score*2}} puntos</div>
            
                                    <!-- </div> -->
                                </div>
                                <div class="row  ">
                                    <!-- <div class="conteiner-general"> -->
                                        <div class="total-score  ">TotalScore = 2 * </div>
                                        <div class="user-score ">{{storeMerits[((call.id-1)*4)].score}}</div>
                                    <!-- </div> -->
                                </div>
                            </div>
                            <div class="merito-conteiner color-change ">
                                <div class="row padding-bottom ">
                                    <div class="merito-number  "><strong>{{storeMerits[((call.id-1)*4)+1].name}}</strong></div>
                                    <div class="puntos-number  ">{{storeMerits[((call.id-1)*4)+1].score*2}} puntos</div>
                                </div>
                                <div class="row  ">
                                    <div class="total-score  ">TotalScore = 2 * </div>
                                    <div class="user-score  ">{{storeMerits[((call.id-1)*4)+1].score}}</div>
                                </div>
                            </div>
                        </div>
                        <div class=" merito-conteiner_wrapper ">
                            <div class="merito-conteiner ">
                                <div class="row padding-bottom ">
                                    <div class="merito-number "><strong>{{storeMerits[((call.id-1)*4)+2].name}}</strong></div>
                                    <div class="puntos-number ">{{storeMerits[((call.id-1)*4)+2].score*2}} puntos</div>
                                </div>
                                <div class="row ">
                                    <div class="total-score ">TotalScore = 2 * </div>
                                    <div class="user-score ">{{storeMerits[((call.id-1)*4)+2].score}}</div>
                                </div>
                            </div>
                            <div class="merito-conteiner color-change ">
                                <div class="row padding-bottom  ">
                                    <div class="merito-number "><strong>{{storeMerits[((call.id-1)*4)+3].name}}</strong></div>
                                    <div class="puntos-number ">{{storeMerits[((call.id-1)*4)+3].score*2}} puntos</div>
                                </div>
                                <div class="row ">
                                    <div class="total-score ">TotalScore = 2 * </div>
                                    <div class="user-score ">{{storeMerits[((call.id-1)*4)+3].score}}</div>
                                </div>
                            </div>
                        </div>
                        </div>
                    
                </div>
            </div>
            
    </div>
    
</template>

<script>
export default {

    computed: {
        storeCalls () {
            const callsFromStore = this.$store.state.calls

            return callsFromStore
        },
        storeMerits () {
            const meritsFromStore = this.$store.state.merits

            return meritsFromStore
        }
    }
  
}
</script>

