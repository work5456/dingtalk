# 相关链接

- [开放平台](https://open-doc.dingtalk.com/microapp/isv)
- [IDE 下载](https://open-doc.dingtalk.com/microapp/kn6zg7)
- [前端 api](https://open-doc.dingtalk.com/microapp/dev)
- [后端 api](https://open-doc.dingtalk.com/microapp/serverapi3)
- [钉钉管理后台](https://oa.dingtalk.com/#/login)

# 自带的 ui 组件

- [表单元素](https://open-doc.dingtalk.com/microapp/dev/button-component)
- [操作反馈(toast、loading、modal、actionsheet)](https://open-doc.dingtalk.com/microapp/dev/ui-feedback)

```js
dd.showToast({
  type: 'success',
  content: '操作成功',
  duration: 3000,
  success: () => {
    dd.alert({
      title: 'toast 消失了'
    })
  }
})
```

- 地图组件(高德地图)

```js
"tabBar": {
    "textColor": "#404040",
    "selectedColor": "#108ee9",
    "backgroundColor": "#F5F5F9",
    "items": [
      {
        "pagePath": "pages/index/index",
        "name": "index"
      },
      {
        "pagePath": "pages/map/map",
        "name": "地图"
      }
    ]
  }
```

# 与 web 开发类比

- [概述](https://open-doc.dingtalk.com/microapp/dev/framework-overview)

- [.axml(html) 视图层(view)](https://open-doc.dingtalk.com/microapp/dev/axml)
- [.acss(css)](https://open-doc.dingtalk.com/microapp/dev/acss)
- .js(交互逻辑处理) 数据层、控制层(model、controller)
- .json(配置 title、背景)
- view 标签(div、span)
- dd 全局变量(window)

# [事件](https://open-doc.dingtalk.com/microapp/dev/events)

# [ajax](https://open-doc.dingtalk.com/microapp/dev/httprequest)

```js
dd.httpRequest({
  url: 'http://httpbin.org/post',
  method: 'POST',
  data: {
    from: '钉钉',
    production: 'Dingtalk'
  },
  dataType: 'json',
  success: function(res) {
    dd.alert({ content: 'success' })
  },
  fail: function(res) {
    dd.alert({ content: 'fail' })
  },
  complete: function(res) {
    dd.hideLoading()
    dd.alert({ content: 'complete' })
  }
})
```

# [文件上传下载](https://open-doc.dingtalk.com/microapp/dev/network)

# [图片](https://open-doc.dingtalk.com/microapp/dev/media-image)

# [缓存(localstorage)](https://open-doc.dingtalk.com/microapp/dev/storage)

# [调用系统功能(查看系统信息、网络状态、扫码、蓝牙、震动、电话)](https://open-doc.dingtalk.com/microapp/dev/system-info)

# [位置](https://open-doc.dingtalk.com/microapp/dev/location)

# [免登录](https://open-doc.dingtalk.com/microapp/dev/wcoaey)

# [开发、发布](https://oa.dingtalk.com/#/login)

# 注意事项

- 由于框架并非运行在浏览器中，所以 JavaScript 在 web 中的一些能力都无法使用，如 document、window 等对象
- 不支持直接的 dom 操作,很多开源 web 组件不能直接移植
- [节点查询](https://open-doc.dingtalk.com/microapp/dev/selector-query)
- [开发自定义组件](https://open-doc.dingtalk.com/microapp/dev/custom-component-overview)
