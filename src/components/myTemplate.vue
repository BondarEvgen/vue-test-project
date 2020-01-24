<template>
    <div>

        <div v-for="call of storeCalls" v-bind:key="call" class="convocaria_conteiner conteiner-general " >
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
                                        <div class="merito-number  "><strong>{{storeMerits[0].name}}</strong></div>
                                        <div class="puntos-number  ">{{storeMerits[0].score*2}} puntos</div>
            
                                    <!-- </div> -->
                                </div>
                                <div class="row  ">
                                    <!-- <div class="conteiner-general"> -->
                                        <div class="total-score  ">TotalScore = 2 * </div>
                                        <div class="user-score ">{{storeMerits[0].score}}</div>
                                    <!-- </div> -->
                                </div>
                            </div>
                            <div class="merito-conteiner color-change ">
                                <div class="row padding-bottom ">
                                    <div class="merito-number  "><strong>{{storeMerits[1].name}}</strong></div>
                                    <div class="puntos-number  ">{{storeMerits[1].score*2}} puntos</div>
                                </div>
                                <div class="row  ">
                                    <div class="total-score  ">TotalScore = 2 * </div>
                                    <div class="user-score  ">{{storeMerits[1].score}}</div>
                                </div>
                            </div>
                        </div>
                        <div class=" merito-conteiner_wrapper ">
                            <div class="merito-conteiner ">
                                <div class="row padding-bottom ">
                                    <div class="merito-number "><strong>{{storeMerits[2].name}}</strong></div>
                                    <div class="puntos-number ">{{storeMerits[2].score*2}} puntos</div>
                                </div>
                                <div class="row ">
                                    <div class="total-score ">TotalScore = 2 * </div>
                                    <div class="user-score ">{{storeMerits[2].score}}</div>
                                </div>
                            </div>
                            <div class="merito-conteiner color-change ">
                                <div class="row padding-bottom  ">
                                    <div class="merito-number "><strong>{{storeMerits[3].name}}</strong></div>
                                    <div class="puntos-number ">{{storeMerits[3].score*2}} puntos</div>
                                </div>
                                <div class="row ">
                                    <div class="total-score ">TotalScore = 2 * </div>
                                    <div class="user-score ">{{storeMerits[3].score}}</div>
                                </div>
                            </div>
                        </div>
                        </div>
                </div>
            </div>
            <div>{{storeMerits[1]}}</div>
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
//   props : {
//     callsFromStore : {
//       type: Array,
//       required: true
//     },
//     meritsFromStore : {
//       type: Array,
//       required: true
//     }
//   }
  
}
</script>

