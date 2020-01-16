### Server

1.  ~~验证码校验接口，手机号校验~~    
    delay
2.  ~~注册接口，手机号与验证码校验~~    
    delay
3.  登录接口，用户名，密码校验     
    url:visual/login/viewLogin    
    method:post    
    param:body    
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
        "validityDate": "2020-01-13",
        "loginName": "admin",    
        "userName": "管理员",    
        "userId": "45473EC8D9FD43B38C1DED24D69398FA",    
        "userCode": "admin",
        "loginNum": 4,
        "createDate": "2020-01-14"  
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
      validityDate:到期时间    
      loginNum:登录次数    
      createDate:创建时间    

4.  ~~忘记密码，即重置密码(1. 可直接与管理员沟通进行修改，2.直接通过验证码修改)~~    
    delay
5.  下载文件时是否需要md5完整性的校验    
    todo
6.  音频信息获取接口    
    todo
7.  音频信息更新校验接口    
    url:visual/misFile/getMisFiles     
    method:post    
    param:无    
    response:    
    ```
    {  
      "success": true,  
      "msg": "获取成功",  
      "obj": [{   
        "id": "musicId"
        "fileName": "music",    
        "fileSize": "2048",
        "pain": 1,
        "createDate": "2020-01-02",
        "updateStatus": 0,
        "plalceSize": 3,    
        "filePath": "http://www.baidu.com"  
      },{   
        "id": "musicId"
        "fileName": "music",    
        "fileSize": "1024",
        "pain": 1,
        "createDate": "2020-01-01",
        "updateStatus": 0,
        "plalceSize": 1,    
        "filePath": "http://www.baidu.com"    
      }]
    }
    ```
    参数说明:    
    success 返回成功   
    msg 返回消息   
    obj 返回结果   
    id 文件id    
    fileName 文件名称   
    fileSize 文件大小   
    pain 疼痛感 1：无痛；2：轻微疼痛；3轻度疼痛；4：中度疼痛；5：重度疼痛；6剧烈疼痛     
    createDate 创建时间       
    updateStatus 更新状态 是否有更新（0否，1是）     
    plalceSize 宫口大小    
     1：<1CM;    
     2:1~3CM;    
     3:3-6CM;    
     4:6-10CM;    
     0:其他    
     filePath:音频在线地址    
8.  下载接口        
    url:visual/misFile/download             
    method:POST         
    param:id：文件ID；fileName：文件名称（需后缀名）    
    response:    
