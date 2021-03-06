# universal-navigate

路由导航能力实现

## 支持
<img alt="browser" src="https://gw.alicdn.com/tfs/TB1uYFobGSs3KVjSZPiXXcsiVXa-200-200.svg" width="25px" height="25px" /> <img alt="weex" src="https://gw.alicdn.com/tfs/TB1jM0ebMaH3KVjSZFjXXcFWpXa-200-200.svg" width="25px" height="25px" /> <img alt="miniApp" src="https://gw.alicdn.com/tfs/TB1bBpmbRCw3KVjSZFuXXcAOpXa-200-200.svg" width="25px" height="25px" /> <img alt="wechatMiniprogram" src="https://img.alicdn.com/tfs/TB1slcYdxv1gK0jSZFFXXb0sXXa-200-200.svg" width="25px" height="25px"> <img alt="quickApp" src="https://gw.alicdn.com/tfs/TB1MP7EwQT2gK0jSZPcXXcKkpXa-200-200.svg" width="25px" height="25px"> <img alt="bytedanceMicroApp" src="https://gw.alicdn.com/tfs/TB1jFtVzO_1gK0jSZFqXXcpaXXa-200-200.svg" width="25px" height="25px">

## Install
```bash
$ npm install universal-navigate --save
```

## Usage
```javascript
import Navigate from 'universal-navigate';

// 快应用中的引入方法
// import chooseImage from 'universal-navigate/lib/quickapp;

Navigate.push({
  url: 'https://www.taobao.com/',
  animated: true // 仅 weex 中支持
}).then(() => {
});

Navigate.pop({
  animated: false // 仅 weex 中支持
}).then(() => {
});

Navigate.go({
  step: -1,
  animated: false // 仅 weex 中支持
}).then(() => {
});

```
## 方法
### `push(options)`

#### 参数
| 成员             | 类型      | 描述                                       | 必选  | 默认值 | 支持  |
| ---------------- | --------- | ------------------------------------------ | :---: | :----: | :---: |
| options          | `object`  | push 参数                                  |  是   |   -    |   -   |
| options.url      | `string`  | 页面 URL.                                  |  是   |   -    |   -   |
| options.animated | `boolean` | 仅weex中支持，页面压入时是否需要动画效果。 |  否   | `true` |<img alt="weex" src="https://gw.alicdn.com/tfs/TB1jM0ebMaH3KVjSZFjXXcFWpXa-200-200.svg" width="25px" height="25px" /> |

### `pop(options)`

#### 参数
| 成员             | 类型      | 描述                                       | 必选  | 默认值 | 支持  |
| ---------------- | --------- | ------------------------------------------ | :---: | :----: | :---: |
| options          | `object`  | pop 参数                                   |  否   |   -    |       |
| options.animated | `boolean` | 仅weex中支持，页面压入时是否需要动画效果。 |  否   | `true` |<img alt="weex" src="https://gw.alicdn.com/tfs/TB1jM0ebMaH3KVjSZFjXXcFWpXa-200-200.svg" width="25px" height="25px" /> |

### `go(options)`

#### 参数
| 成员             | 类型      | 描述                                                                                | 必选  | 默认值 | 支持  |
| ---------------- | --------- | ----------------------------------------------------------------------------------- | :---: | :----: | :---: |
| options          | `object`  | go 参数                                                                             |  是   |   -    |       |
| options.step     | `number`  | 前进步数为正值且仅支持web，后退步数为负值，若大于现有打开的页面数，则返回到起始页。 |  是   |   -    |       |
| options.animated | `boolean` | 仅weex中支持，页面压入时是否需要动画效果。                                          |  否   | `true` |<img alt="weex" src="https://gw.alicdn.com/tfs/TB1jM0ebMaH3KVjSZFjXXcFWpXa-200-200.svg" width="25px" height="25px" />|

