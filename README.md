
# ElementUI2 通用库

> 先这样规划，待完成。


## 1.函数

- 安装

```
npm install elementui-w-util
```

- 函数

|函数|功能|备注|
|---|---|---|
|getCookieUtil|获取cookie|@..|
|PhoneValidator|验证固定电话|8位号码0411-84720021、041184720021、84720021或7位号码|
|MobileValidator|验证手机号码|1~3·4·5·6·7·8·9~xxx，共11位|
|IdCardValidator|验证身份证|18位，最后一位可以是x|


- 使用

```js
// 引入
import { getCookieUtil } from 'elementui-w-util'

// 使用
export default {
  methods: {
    getCookieUtil,
    getUserList() {
      this.getCookieUtil...
    }
  }
}
```



## 2.验证器

- 安装

```
npm install elementui-w-validator
```

- 验证器：min、max、length框架自带了

|验证器|功能|备注|
|---|---|---|
|emailValidator|验证邮箱|@..|
|phoneValidator|验证固定电话|8位号码0411-84720021、041184720021、84720021或7位号码|
|mobileValidator|验证手机号码|1~3·4·5·6·7·8·9~xxx，共11位|
|idCardValidator|验证身份证|18位，最后一位可以是x|


- 使用

```js
// 引入
import { emailValidator } from 'elementui-w-validator'

// 使用
export default {
  data () {
    return {
      emailValidator,
      rules: {
        mail: [ {trigger: "blur", validator: emailValidator} ]
      }
    }
  }
}
```



## 3.自定义指令

- 安装

```
npm install elementui-w-directive
```

- 指令

|指令|功能|备注|
|---|---|---|
|turnToNum|输入非数字清空，输入数字保留2为小数|@..|
|phoneValidator|验证固定电话|8位号码0411-84720021、041184720021、84720021或7位号码|
|mobileValidator|验证手机号码|1~3·4·5·6·7·8·9~xxx，共11位|
|idCardValidator|验证身份证|18位，最后一位可以是x|


- 使用

```vue
// 使用
<el-input v-model="searchForm.price" v-turnToNum placeholder="请输入价格"></el-input>

// 引入（可以全局导入）
import 'elementui-w-directive'
```



## 4.过滤器

当成**转换器**用

- 安装

```
npm install elementui-w-filter
```

- 过滤器

|过滤器|功能|备注|
|---|---|---|
|operateTimeFilter|验证邮箱|@..|
|phoneValidator|验证固定电话|8位号码0411-84720021、041184720021、84720021或7位号码|
|mobileValidator|验证手机号码|1~3·4·5·6·7·8·9~xxx，共11位|
|idCardValidator|验证身份证|18位，最后一位可以是x|


- 使用

```vue
// 使用
<el-table-column prop="operateTime" label="创建日期" min-width="120">
  <template slot-scope="scope">{{ scope.row.operateTime | operateTimeFilter }}</template>
</el-table-column>

// 引入
import { operateTimeFilter } from 'elementui-w-filter'

// 使用
export default {
  methods: {
    operateTimeFilter
  }
}
```