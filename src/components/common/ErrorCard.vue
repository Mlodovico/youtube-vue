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
    <div class="card-error-wrapper">
        <div>
            <p class="title" v-if="!title"> Something went wrong with the server =( </p>
            <p class="title" v-else> {{ title }} </p>
        </div>
    </div>
</template>

<style>

.card-error-wrapper {
    min-width: 50vh;
    min-height: 20svh;
    display: flex;
    flex-direction: center;
    align-items: center;
    text-align: center;
    border-radius: 10px;
    border-width: 2px;
    border-style: solid;
    border-color: rgb(75, 75, 75);
    justify-content: center;
    align-items: center;
    font-weight: bold;
    margin-top: 20svh
}

.title {
    font-size: 16px;
    font-weight: bold;
    margin-bottom: 5px;
}

</style>