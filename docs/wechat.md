# 基础方法使用  

###### 企业微信发送前置条件  
开通企业微信：https://work.weixin.qq.com/  

###### sendMsgToWechat(发送消息到企业微信)  
> 传入参数  
> corpid：企业id  
> corpsecret：企业应用的Secret  
> topartyid：企业应用通知的部门id  
> agentid：企业应用的AgentId  
> msg：发送的消息内容  
> 返回参数  
> num：0成功，-1失败  

调用示例：  
```python  
class Test:
    def __init__(self):
        self.wx = SendWechatMsg()
    def test(self):
        result = self.wx.sendMsgToWechat(企业id,企业secret,部门id,企业AgentId,'发送的消息内容')
```  
