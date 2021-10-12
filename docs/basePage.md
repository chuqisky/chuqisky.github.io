# 基础方法使用  

###### base_find_elt(单个元素定位)  
> 传入参数  
> driver：浏览器对象  
> location：定位元素  
> timeout：最大等待时间  
> poll：检查频率  
> 返回参数  
> object：元素对象  

调用示例：  
```python  
class Test(BasePage):
    def __init__(self):
        # 得到浏览器对象
        self.driver = DriverUtil.get_driver('chrome',True)
    def test(self):
        return self.base_find_elt(self.driver,(By.ID,'ID'))
```  

###### base_find_elts(多个元素定位)  
> 传入参数  
> driver：浏览器对象  
> location：定位元素  
> timeout：最大等待时间  
> poll：检查频率  
> 返回参数  
> list{object}：元素对象集合  

调用示例：  
```python  
class Test(BasePage):
    def __init__(self):
        # 得到浏览器对象
        self.driver = DriverUtil.get_driver('chrome',True)
    def test(self):
        return self.base_find_elts(self.driver,(By.CLASS_NAME,'class_name'))
```  

###### base_isExsit_elt(判断元素是否存在)  
> 传入参数  
> driver：浏览器对象  
> location：定位元素  
> timeout：最大等待时间  
> poll：检查频率  
> 返回参数  
> bool：true或false

调用示例：  
```python  
class Test(BasePage):
    def __init__(self):
        # 得到浏览器对象
        self.driver = DriverUtil.get_driver('chrome',True)
    def test(self):
        result = self.base_isExsit_elt(self.driver,(By.CLASS_NAME,'class_name'))
```  

###### base_find_el_by_fatherEL(通过父类元素查找单个元素)  
> 传入参数  
> driver：浏览器对象  
> fatherEL：父元素对象  
> location：定位元素  
> timeout：最大等待时间  
> poll：检查频率  
> 返回参数  
> object：元素对象

调用示例：  
```python  
class Test(BasePage):
    def __init__(self):
        # 得到浏览器对象
        self.driver = DriverUtil.get_driver('chrome',True)
    def test(self):
        # 得到父元素对象
        father = self.base_find_elt(self.driver,(By.CLASS_NAME,'class_name'))
        return self.base_find_el_by_fatherEL(self.driver,father,(By.NAME,'name'))
```  

###### base_find_els_by_fatherEL(通过父类元素查找多个元素)  
> 传入参数  
> driver：浏览器对象  
> fatherEL：父元素对象  
> location：定位元素  
> timeout：最大等待时间  
> poll：检查频率  
> 返回参数  
> list{object}：元素对象集合

调用示例：  
```python  
class Test(BasePage):
    def __init__(self):
        # 得到浏览器对象
        self.driver = DriverUtil.get_driver('chrome',True)
    def test(self):
        # 得到父元素对象
        father = self.base_find_elt(self.driver,(By.CLASS_NAME,'class_name'))
        return self.base_find_els_by_fatherEL(self.driver,father,(By.NAME,'name'))
```  

###### base_swith_window(切换窗口/句柄)  
> 传入参数  
> driver：浏览器对象  
> num：窗口列表中的第几个窗口  
> 返回参数（无）  

调用示例：  
```python  
class Test(BasePage):
    def __init__(self):
        # 得到浏览器对象
        self.driver = DriverUtil.get_driver('chrome',True)
    def test(self):
        self.base_swith_window(self.driver,1)
```  