<template>
    <div class="card-wrapper">
        <div class="video-content">
            <p>Content</p>
        </div>
        <div class="text-content">
            <p>Como fazer bolo de cenoura</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CardComponent'
}
</script>

<style>
.card-wrapper {
    width: 300px;
    height: 300px;
    display: flex;
    flex-direction: column;
    background: black;
    border-radius: 10px;
}

.video-content {
    width: 100%;
    height: 50%;
    border-radius: 10px 10px 0 0;
}

.text-content {
    width: 100%;
    height: 50%;
    border-radius: 0 0 10px 10px;
    color: white;
    font-weight: bold;
    padding: 10px;
}
</style>