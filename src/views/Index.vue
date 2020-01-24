<template>
  <div>
    <div class="conteiner ">

        <myTemplate ></myTemplate>
        
    </div>
  </div>
</template>

<script>

import myTemplate from '@/components/myTemplate'

export default {
    components : {
        myTemplate
    },
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