# spa-redux-tool
### 动机
  一个重新包装过的redux，提高开发效率

### 使用

```javascript
  import registerEkko, { Provider } from 'spa-redux-tool'
  import allModel from '@/model'  // 所有model集合
  const store = registerEkko(allModel)
  ReactDOM.render(
    <Provider store={store}>
      <App />
    </Provider>
    , document.getElementById('root'))
```

### 约定
  model中必须三个属性 
  - namespace: string  对该 model 进行唯一识别
  - state: object      model 的状态值容器
  - reducers: Function{} 

### model中API
- setState 改变状态值
- getModelState 获取当前所在 model的状态
- getState 获取所有 model 的状态
- resetState 重置当前 model 的状态

## Change Log
