# Vue 高级特性

## 自定义 `v-model`

## `$nextTick`

- Vue 是异步渲染的
- data 改变之后，DOM 不会立刻渲染
- `$nextTick` 会在 DOM 渲染之后被触发，以获取最新 DOM 节点

## slot

- 基本使用
- 作用域插槽
- 具名插槽

## 动态组件

- `:is="component-name"` 用法
- 需要根据数据，动态渲染的场景。即组件类型不确定。
- 比如新闻文章页，不确定多少个段落、视频、图片。

## 异步组件

- `import()` 函数
- 按需加载，异步加载大组件

## keep-alive

- 缓存组件
- 频繁切换，不需要重复渲染

## mixin

- 多个组件有相同的逻辑，抽离出来
- mixin 并不是完美的解决方案，会有一些问题
- Vue 3 提出的 Composition API 旨在解决这些问题

### mixin 问题

- 变量来源不明确，不利于阅读
- 多 mixin 可能会造成命名冲突
- mixin 和组件可能出现多对多的关系，复杂度较高