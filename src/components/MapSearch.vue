<template>
    <div>
        <div id="container"></div>
        <div id="panel"></div>
    </div>
</template>

<script>
import AMapLoader from '@amap/amap-jsapi-loader';

export default {
    mounted() {
        window._AMapSecurityConfig = {
            securityJsCode: "ed44fa0f4256e6f54aba8b03a1450970",
        };
        AMapLoader.load({
            key: "6e747115bd5e50ddd7cf202995156893", // 申请好的Web端开发者Key，首次调用 load 时必填
            version: "2.0", // 指定要加载的 JSAPI 的版本，缺省时默认为 1.4.15
            plugins: ["AMap.PlaceSearch"], //需要使用的的插件列表，如比例尺'AMap.Scale'，支持添加多个如：['...','...']
        }).then(() => {
            //地图加载
            var map = new AMap.Map("container", {
                resizeEnable: true
            });

            AMap.plugin(["AMap.PlaceSearch"], () => {
                // 构造地点查询类
                var placeSearch = new AMap.PlaceSearch({
                    pageSize: 5, // 单页显示结果条数
                    pageIndex: 1, // 页码
                    city: "", // 兴趣点城市
                    citylimit: true,  // 是否强制限制在设置的城市内搜索
                    map: map, // 展现结果的地图实例
                    panel: "panel", // 结果列表将在此容器中进行展示。
                    autoFitView: true // 是否自动调整地图视野使绘制的 Marker点都处于视口的可见范围
                });
                // 关键字查询
                placeSearch.search('武汉神州租车');
            });
        }).catch(e => {
            console.error(e);
        });
    }
}
</script>

<style scoped>
#container {
    width: 100%;
    height: 100%;
}

#panel {
    position: absolute;
    background-color: white;
    max-height: 90%;
    overflow-y: auto;
    top: 10px;
    right: 10px;
    width: 280px;
}
</style>