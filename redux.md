# redux
Redux 是 JavaScript 状态容器，提供可预测化的状态管理。
Redux 单向数据流（用户行为和系统响应的抽象，能更好处理复杂交互，让state变得可预测）
Redux简单小，压缩后2kb，单一状态树。
React是纯View层，需要数据流支撑。
Redux 安装 `npm install react-redux redux`

## reducer
1. 是响应的抽象
2. 是纯方法（不依赖系统时间）
3. 传入旧状态和action
4. 返回新state

Store（包含所有reducer）各个reducer和state的集合

state是运行时才有的，我们定义好的只有reducer，Store其实由redux里面createStore方法生成的。我们调用createStore把所有的reducer传进去得到store

action作用store
reducer根据store响应
store是唯一的
store包括了完整的state
state变得完全可以预测

## container和component区别

| Property / Type | Container | Component |
| - | - | - |
| 目的 | 如何工作（数据获取，状态更新） | 如何显示（样式，布局） |
| 是否在Redux数据流中 | 是 | 否 |
| 读取数据 | 从Redux获取State | 从props获取数据 |
| 修改数据 | 向Redux派发actions | 从props 调用回调函数 |
| 实现方式 | 由react-redux生成 | 手写 |
|  复用性 | 业务逻辑这块难复用 | 纯展示，易复用 |
