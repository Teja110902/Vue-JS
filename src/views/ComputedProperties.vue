<template>
    <div>
        <h1>Computed Properties</h1>
        <input type="text" placeholder="First Name" v-model="fname">
        <br /> <br />
        <input type="text" placeholder="Last Name" v-model="lname">

        <h1>Welcome {{ fullName }} </h1>
    </div>
</template>

<script>
export default {
    data() {
        return {
            fname: "",
            lname: ""
        }
    },

    computed: {
        fullName() {
            return this.fname + " " + this.lname
        }
    },
}
</script>

<style lang="scss" scoped>

</style>