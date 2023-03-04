<template>
    <div>
        <h1>Computed Properties Setter Example</h1>
        <input type="text" placeholder="Firstname" v-model="fname">
        <br><br>
        <input type="text" placeholder="Lastname" v-model="lname">
        <br><br>
        <input type="text" placeholder="Fullname" v-model="fullName">
        <br><br>
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
        // The below notation is used when we want computed property as only a getter
        // fullName() {
        //   return this.fname + " " + this.lname
        // }
        fullName: {
            get() {
                return this.fname + " " + this.lname
            },
            set(newValue) {
                let names = newValue.split(' ');
                this.fname = names[0];
                this.lname = names[names.length - 1];
            }
        }
    },
}
</script>

<style lang="scss" scoped>

</style>