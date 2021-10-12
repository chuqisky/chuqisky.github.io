# 基础方法使用  

###### 日志功能介绍  
系统中新建logUtils对象，会自动在项目log文件夹下生成对应日志文件，日志仅支持debug、info、warning、error、critical五种日志类型。  

###### logging_msg(根据日志类型写入日志)  
> 传入参数  
> type：日志类型（debug、info、warning、error、critical）  
> msg：日志消息  
> exception：异常信息，只在warning、error、critical级别日志会打印  
> 返回参数（无）  

调用示例：  
```python  
class Test:
    def __init__(self):
        self.logs = LogUtils()
    def test(self):
        self.logs.logging_msg('error','测试xxx异常','自定义异常')
```  