<script>
export default {
    name: 'CardComponent',
    props: {
        video: {
            type: Object,
            required: true
        },
    }
}
</script>

<template>
    <div class="card-wrapper">
        <div class="video-content">
            <img :src="video.img" alt="">
        </div>
        <div class="text-content">
            <div class="profile-wrapper"></div>
            <div class="content">
                <p class="title">{{ video.title }}</p>
                <p class="author">{{ video.author }}</p>
                <p class="description">{{ video.description }}</p>
            </div>
        </div>
    </div>
</template>
<style>
.card-wrapper {
    width: 300px;
    height: 220px;
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

.video-content img {
    width: 100%;
    height: 100%;
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
.title {
    font-size: 16px;
    font-weight: bold;
    margin-bottom: 5px;
}

.author {
    font-size: 14px;
    color: gray;
}

.description {
    font-size: 12px;
    color: gray;
}
</style>