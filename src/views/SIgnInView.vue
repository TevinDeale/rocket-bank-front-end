<script setup>
import LoginForm from '@/components/Login-Form.vue';

</script>

<template>
    <section class="sign-in-container">
        <LoginForm />
    </section>  
</template>

<style lang="scss" scoped>
.sign-in-container, .create-account-container{
    min-height: 100vh;
    width: 100%;
    display: flex;
    justify-content: center;
}
</style>