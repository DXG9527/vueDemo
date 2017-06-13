<template>
    <div id="secondComponent">
        <el-carousel :interval="4000" type="card" height="200px">
            <el-carousel-item v-for="article in articles" :key="article">
                <h3>{{ article.menuName }}</h3>
            </el-carousel-item>
        </el-carousel>
        <!--<ul>-->
            <!--<li v-for="article in articles">-->
                <!--{{article.menuName}}-->
            <!--</li>-->
        <!--</ul>-->
    </div>
</template>
<script>
    import axios from 'axios'
    export default{
        data() {
            return {
                articles : []
            }
        },
        mounted: function () {
            axios.get('https://dev.ud.itt.space/ud-app-service/ud/menu')
                .then((result) => {
                    this.articles = result.data.data;
                    console.log(result);
                })
        }
    }
</script>
<style>
    .el-carousel__item h3 {
        color: #475669;
        font-size: 14px;
        opacity: 0.75;
        line-height: 200px;
        margin: 0;
    }

    .el-carousel__item:nth-child(2n) {
        background-color: #99a9bf;
    }

    .el-carousel__item:nth-child(2n+1) {
        background-color: #d3dce6;
    }
</style>