<template>
    <div>
        <input v-model="firstName" placeholder="First Name">
        <input v-model="lastName" placeholder="Last Name">
        {{fullName}}
        {{incrementOne}}
    </div>
</template>
<script>

export default {
    data() {
        return {
            firstName:"",
            lastName: "",
            count: 0
        }
    },
    computed: {
        fullName(){
            return `${this.firstName}   ${this.lastName}`;
        },
        incrementOne: {
            get(){
                return this.count+1;
            },
            set(val){
                this.count = val -1;
            }
        }
    }
}
</script>