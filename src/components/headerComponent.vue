<template>
    <div id="headerComponent">
        <el-menu theme="dark" :default-active="activeIndex" class="el-menu" mode="horizontal" @select="handleSelect">
            <el-menu-item index="1"><router-link to="/first">第一页</router-link></el-menu-item>
            <el-menu-item index="2"><router-link to="/second">第二页</router-link></el-menu-item>
        </el-menu>
        <router-view class="view"></router-view>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                activeIndex: '1'
            };
        },
        methods: {
            handleSelect(key, keyPath) {
                console.log(key, keyPath);
            }
        }
    }
</script>

<style>
    .el-menu {
        padding-left: 55px;
        background-color: #324157;
        border-radius: 2px;
        position: relative;
        margin: 0;
        width: 1400px;
    }
    .el-menu:before {
        display: table;
        content: "";
    }
    .el-menu:after {
        clear: both;
    }
    .el-menu:after, .el-menu:before {
        display: table;
        content: "";
    }
</style>