<template>
    <div class="container">
        <h3 class="mb-2"> {{counter}} </h3>
        <button class="red sm">-</button>
        <button class="green sm">+</button>
    </div>
</template>

<script>
export default{
    data(){
        return{
            counter:0,
        }
    }
}
</script>