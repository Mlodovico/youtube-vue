<script>
export default {
    name: 'SideBarComponent',

    data() {
        return {
            search: ''
        }
    },

    methods: {
        onClick() {

        }
    }
}
</script>

<template>
    <div class="side-bar-container">
        <div class="items-list">

        </div>
    </div>
</template>

<style>
.side-bar-container {
    width: 30%;
    height: 100vh;
    top: 0;
        left: 0;
        position: absolute;
    background-color: rgb(30, 30, 30);
    @media screen and (width >=1366px) {
            width: 20%;
        }
    
        @media screen and (width <=900px) {
            width: 30%;
        }
    
        @media screen and (width <=600px) {
            width: 100%;
        }
}
</style>