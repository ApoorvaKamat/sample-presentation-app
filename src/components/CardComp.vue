<template>
    <div class="card" style="width: 18rem;">
        <img alt="Vue logo" src="../assets/logo.png">
        <div class="card-body">
            <h5 class="card-title">{{ title }}</h5>
            <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's
                content.</p>
            <button type="button" class="btn btn-primary" data-bs-toggle="modal" :data-bs-target="`#${modalId}`">
                Click to view more ...
            </button>
        </div>
    </div>
    <modal-comp :id="modalId"></modal-comp>
</template>

<script>
// import { computed, ref } from 'vue';
import ModalComp from './ModalComp.vue';
export default {
    name: 'CardComp',
    props: {
        title: String,
        text: String
    },
    components:{
        ModalComp,
    },
    data(){
        return {
            modalId: 'desc-modal'
        }
    },
    methods:{
        getModalTitle(){
            return this.title;
        }
    }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>