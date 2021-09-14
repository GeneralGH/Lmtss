<template>
    <div class="beian">
        <a href="https://beian.miit.gov.cn/" target="_blank">
        苏ICP备2021041003号-1
        </a>
    </div>
</template>

<script>
export default {
    name:'BeiAn',
    setup() {
        
    }
}
</script>

<style lang="scss">
.beian {
    background: none;
    height: 5%;
    bottom: 0;
    width: 100%;
    position: fixed;
    text-align: center;
}
a {
    font-family:Arial, Helvetica, sans-serif;
    text-decoration: none;
    color: rgba(255, 255, 255, 0.815);
    cursor: pointer;
    transition: .25s;
    opacity: 0.7;
    font-size: 13px;
    &:hover {
        opacity: 1;
    }
}
</style>