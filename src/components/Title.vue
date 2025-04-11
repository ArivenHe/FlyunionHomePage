<script>
    export default {
        name: "Title",
        data() {
            return {};
        },
        props: {
            text: "",
        },
    };
</script>
<template>
    <p>{{ text }}</p>
</template>

<style scoped>
    p {
        font-size: 8vh;
        font-weight: 600;
        background-clip: text;
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-image: linear-gradient(
            90deg,
            rgb(255, 167, 69),
            rgb(254, 134, 159),
            rgb(239, 122, 200),
            rgb(160, 131, 237),
            rgb(67, 174, 255),
            rgb(160, 131, 237),
            rgb(239, 122, 200),
            rgb(254, 134, 159),
            rgb(255, 167, 69)
        );
        background-size: 200%;
        animation: streamer 5s linear infinite;
    }
    @keyframes streamer {
        0% {
            background-position: 0%;
        }

        100% {
            background-position: 200%;
        }
    }
</style>
