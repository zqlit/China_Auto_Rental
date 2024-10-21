<template>
    <div class="map-container">
        <template>
            <div id="container"></div>
        </template>
    </div>
</template>

<script>
import AMapLoader from '@amap/amap-jsapi-loader';

export default {
    name: 'MapContainer',
    mounted() {
        this.initAMap();
    },
    unmounted() {
        this.map?.destroy();
    },
    methods: {
        initAMap() {
            window._AMapSecurityConfig = {
                securityJsCode: "ed44fa0f4256e6f54aba8b03a1450970",
            };
            AMapLoader.load({
                key: "6e747115bd5e50ddd7cf202995156893", // 申请好的Web端开发者Key，首次调用 load 时必填
                version: "2.0", // 指定要加载的 JSAPI 的版本，缺省时默认为 1.4.15
                plugins: ["AMap.Scale"], //需要使用的的插件列表，如比例尺'AMap.Scale'，支持添加多个如：['...','...']
            })
                .then((AMap) => {
                    this.map = new AMap.Map("container", {
                        // 设置地图容器id
                        viewMode: "3D", // 是否为3D地图模式
                        zoom: 11, // 初始化地图级别
                        center: [116.397428, 39.90923], // 初始化地图中心点位置
                    });
                })
                .catch((e) => {
                    console.log(e);
                });
        },
    },
};
</script>

<style scoped>
.map-container {}

#container {
    padding: 0px;
    margin: 0px;
    width: 100%;
    height: 800px;
}
</style>