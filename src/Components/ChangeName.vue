<template>
    <div class="change-name">
        <h1>{{ message }}</h1>
        <input type="text" v-model="message" placeholder="here name's">
    </div>
</template>

<script>
export default{
    data(){
        return{
            message: ""
        }
    }
}
</script>