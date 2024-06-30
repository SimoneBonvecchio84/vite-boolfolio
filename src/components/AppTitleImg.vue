<script>
export default {
    data () {
        return {
            title: "Simone"
        }
    }
}
</script>

<template>
    <div class="container">
        <h2>{{ title }}</h2>
        <img src="../assets/img/simo.jpg" alt="">
    </div>

</template>

<style>
    h2 {
       position: absolute;
       color:white;
       top: 50%;
       left: 50%;
       transform: translate(-50%, -50%);
       font-size: 3rem;
    }
    .container {
        position: relative;

    }
    .container img {
        width: 100%;
    }
</style>