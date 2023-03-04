<template>
    <div>
        <h1>Welcome to Watchers</h1>
        <input type="text" placeholder="Firstname" v-model="fname">
        <br><br>
        <input type="text" placeholder="Lastname" v-model="lname">
        <h1>You full name is {{ fullName }}</h1>
    </div>
</template>

<script>
export default {
    data() {
        return {
            fname: "",
            lname: "",
            fullName: ""
        }
    },
    watch: {
        fname(newValue, oldValue) {
            this.fullName = newValue + " " + this.lname;
        },

        lname(newValue, oldValue) {
            this.fullName = this.fname + " " + newValue;
        }
    },
}
</script>

<style lang="scss" scoped>

</style>