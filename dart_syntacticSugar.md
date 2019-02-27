### dart语言语法糖

a、 以 _命名的变量或函数为强制私有

var _num;

b、 支持箭头函数,但后面不能接代码段，只能接受返回值 和 表达式

```

int getInt() => 2;

int getInt() => isTrue ? 2 : 0;

```

c、 运算符

aa ?? bb; ?? 为null 时


d、异步 

async await then

async、await使用与rn中使用方式一致

.then也是异步操作

```
/// 设置需要填写的内容
    _setDefaultData(List<dynamic> list) {
      Future<String> jsonStr = DefaultAssetBundle.of(context).loadString("json/billcontent.json");
      List<dynamic> list1 = [];

      /// 对jsonStr数据做解析
      jsonStr.then((value) {
        var data = json.decode(value);
        if(list != null || list.length > 0) {
          data = list;
        }
        print('data ====' + data.toString());
        data.forEach((item) {
          if(item['type'] == '1') {
            list1.add(item);
          }
        });
      });

      print('list1======' + list1.toString());
      this.setState(() {
        this.saveList = list1;
      });

    }


```
如图这种代码会先输出list1的信息，然后在输出data的信息
说明jsonStr.then 为异步操作