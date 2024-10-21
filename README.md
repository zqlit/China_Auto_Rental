# 神州租车PC Web页面

基于Vue2实现的纯前端项目

## 介绍
该项目是一个神州租车的PC网页，完全基于Vue2实现。应用提供了响应式和用户友好的界面用于租车服务。

## 特性
- 用户认证和授权
- 汽车搜索和过滤
- 预订和预约管理
- 与外部API集成以获取数据
- 响应式设计适用于各种屏幕尺寸

## 使用技术
- Vue2
- Vue Router
- Vuex
- Axios
- Webpack
- Babel

## 项目设置
按照以下步骤在本地设置项目：

1. 克隆仓库：
    ```bash
    git clone https://github.com/zqlit/China_Auto_Rental.git
    cd China_Auto_Rental
    ```

2. 安装依赖：
    ```bash
    npm install
    ```

3. 编译并热加载用于开发：
    ```bash
    npm run serve
    ```

4. 编译并压缩用于生产：
    ```bash
    npm run build
    ```

## 自定义配置
更多详细的配置选项，请参考 [Vue CLI 配置参考](https://cli.vuejs.org/config/)。

## 使用方法
1. 打开浏览器并导航到开发服务器地址，通常为 `http://localhost:8080`。
2. 注册或登录以访问全部功能。
3. 搜索可用车辆，根据需要进行过滤，并进行预订。

## 贡献
我们欢迎对项目的改进做出贡献。请按照以下步骤进行贡献：

1. Fork 仓库。
2. 为您的功能或修复创建一个新分支：
    ```bash
    git checkout -b feature/your-feature-name
    ```
3. 进行更改并提交描述性信息：
    ```bash
    git commit -m "Add feature: your-feature-name"
    ```
4. 将您的分支推送到您的Fork仓库：
    ```bash
    git push origin feature/your-feature-name
    ```
5. 创建一个 Pull Request 到主仓库。

## 许可证
该项目使用 MIT 许可证。详情请参阅 [LICENSE](LICENSE) 文件。
