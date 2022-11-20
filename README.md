# 项目

## 技术架构

- Vue3
- Pinia
- Axios
- VueRouter

## 目录分层

- src(源码)
  - api
  - assets
    - icons
    - svg
    - images
  - base-ui(基础组件)
  - config
  - comstant
  - router
  - components
  - hooks
  - store
  - views
  - service
  - styles
  - utils
  - global(全局按需引入第三方组件库)
  - \*.d.ts(解决 tsline 2307)

## 前端开发规范

## 按需倒入 Element Plus 组件

1. 安装

   ```
   npm install -D unplugin-vue-components unplugin-auto-import

   ```

2.在 vite.config.ts 中配置 plugin

```
# 倒入模块
import AutoImport from "unplugin-auto-import/vite";
import Components from "unplugin-vue-components/vite";
import { ElementPlusResolver } from "unplugin-vue-components/resolvers";

# 引用
plugins: [
    vue(),
    AutoImport({
      resolvers: [ElementPlusResolver()],
    }),
    Components({
      resolvers: [ElementPlusResolver()],
    }),
  ],
```
