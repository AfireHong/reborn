# Store

store是用于全局存储Model实例的集合，后续会在Model中提供跨Model引用的模式。

## 创建Store
创建一个Store，并绑定app使用
:::warning
`beta`功能，后续可能会使用`app.use(store)`的方式来注册
:::
```typescript
import { createStore } from 'vue-apollo-model';
import Vue from 'Vue';

const store = createStore();

store.install(Vue, app);
```
## 注册Rest/GQL对应的Client
注册对应client，**注意** client为单例模式
```typescript
// 注册Rest Client
store.registerClient('REST', restClient);
// 注册GQL Client，暂不可用
store.registerClient('GQL', restClient);
```