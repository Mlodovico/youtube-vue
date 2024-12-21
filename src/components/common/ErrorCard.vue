<script>
export default {
    name: 'ErrorCard',
    props: {
        title: {
            type: String,
            required: false,
        },
    }
}
</script>

<template>
    <div class="card-wrapper">
        <div>
            <p class="title" v-if="!title"> Something went wrong with the server =( </p>
            <p class="title" v-else> {{ title }} </p>
        </div>
    </div>
</template>

<style>

.card-wrapper {
    width: 450vh;
    display: flex;
    flex-direction: center;
    align-items: center;
    text-align: center;
    border-radius: 10px;
    border-width: 3px;
    border-style: solid;
    border-color: rgb(75, 75, 75);
    justify-content: center;
    align-items: center;
    font-weight: bold;
    background-color: white;
}

.title {
    font-size: 16px;
    font-weight: bold;
    margin-bottom: 5px;
}

</style>