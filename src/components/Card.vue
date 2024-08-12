<template>
    <div class="card-wrapper">
        <div class="video-content">
            <p>Content</p>
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

<style>
.card-wrapper {
    width: 300px;
    height: 200px;
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