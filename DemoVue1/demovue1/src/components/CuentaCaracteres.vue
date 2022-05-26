<template>
    <div>
        <input type="text" name="input" id="input" v-model="textoCaja">
        <p>{{cuenta}}</p>
    </div>
</template>
<script>

export default {
    data() {
        return {
        cuenta: 0,
        textoCaja: ""
        }
    },
    methods: {
        contar: function () {
            
        }
    },
    watch: {
        textoCaja() {
        this.cuenta  = this.textoCaja.length;
        
        }
    }
}
</script>