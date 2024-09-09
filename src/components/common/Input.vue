<template>
    <div>
        <input type="text" placeholder="Search" class="search" id="search" v-model="search" @input="onInput">
        <button class="search-button">Search</button>
    </div>
</template>

<script>
export default {
    name: 'InputComponent',
    data() {
        return {
            search: ''
        }
    },
    methods: {
        onInput() {
            this.$emit('search', this.search)
        }
    }
}
</script>

<style>
.search {
    width: 20vw;
    border-radius: 10px 0 0 10px;
    outline: none;
    border: none;
    padding: 10px;
    background-color: rgb(30, 30, 30);
    color: white;
}

.search-button {
    border-radius: 0px 10px 10px 0px;
    border: none;
    padding: 10px 20px;
    background-color: rgb(75, 75, 75);
    color: white;
    font-weight: bold;
    cursor: pointer;
}
</style>