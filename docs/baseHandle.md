# 基础方法使用  

###### base_input(元素输入操作)  
> 传入参数  
> element：元素对象  
> text：输入文本  
> 返回参数（无）  

调用示例：  
```python  
class Test(BaseHandle):
    def test(self):
        self.base_input(元素对象object,'这是输入内容')
```  

###### base_click(元素点击操作)  
> 传入参数  
> element：元素对象  
> 返回参数（无） 

调用示例：  
```python  
class Test(BaseHandle):
    def test(self):
        self.base_click(元素对象object)
```  

###### base_getText(获取元素文本信息)  
> 传入参数  
> element：元素对象  
> 返回参数（无） 

调用示例：  
```python  
class Test(BaseHandle):
    def test(self):
        self.base_getText(元素对象object)
```  

###### base_getIndex_by_elements_text(通过文本判断元组中相同元素，并输出下标)  
> 传入参数  
> elements：元素对象集合
> text：判断文本内容  
> 返回参数  
> number：元素在集合中的下标数字

调用示例：  
```python  
class Test(BaseHandle):
    def test(self):
        self.base_getIndex_by_elements_text(元素对象object,'比对文本')
```  

###### base_move_to_element(鼠标移上)  
> 传入参数  
> driver：浏览器对象  
> element：元素对象 
> condition：判断是否点击（true/false）  
> 返回参数（无）  

调用示例：  
```python  
class Test(BaseHandle):
    def __init__(self):
        # 得到浏览器对象
        self.driver = DriverUtil.get_driver('chrome',True)
    def test(self):
        self.base_move_to_element(self.driver,元素对象object,True)
```  