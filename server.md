### Server

1.  ~~验证码校验接口，手机号校验~~    
    delay
2.  ~~注册接口，手机号与验证码校验~~    
    delay
3.  登录接口，用户名，密码校验     
    url:visual/login/viewLogin    
    method:post    
    param:    
    ```
    {
      loginName:"user",
      password:"md5加密"
    }
    ```
    response:    
    ```
    {  
      "success": true,  
      "msg": "登录成功",  
      "obj": {    
        "loginName": "admin",    
        "userName": "管理员",    
        "userId": "45473EC8D9FD43B38C1DED24D69398FA",    
        "userCode": "admin"  
      }
    }
    ```    
     参数说明   
      success 返回成功  
      msg 返回消息  
      obj 返回结果  
      loginName 登录名  
      userName 姓名  
      userId Id  
      userCode 用户编号 暂时无用

4.  ~~忘记密码，即重置密码(1. 可直接与管理员沟通进行修改，2.直接通过验证码修改)~~    
    delay
5.  下载文件时是否需要md5完整性的校验    
    todo
6.  音频信息获取接口    
    todo
7.  音频信息更新校验接口    
    todo
