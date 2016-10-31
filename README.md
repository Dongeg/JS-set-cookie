# webstroge



这里主要讨论一下几种web存储方式

<h3>cookie</h3>


设置cookie的方法

//在本地可以用火狐浏览器测试<br>

//this example should be running in a server condition

cookie的存储形式
```
arrial=1; wocap=nima
```
具体设置方法参见cookie.html

<h3>localstorage</h3>

localStorage 方法存储的数据没有时间限制

使用方法
```js
    //  设置 localStorage
    function setLocalStorage(key,val){
        return localStorage.setItem(key,val)
    } 
    // 获取 localStorage
    function getLocalStorage(key){
        return localStorage.getItem(key)
    } 
    //删除
    function removeLocalStorage(key){
        return localStorage.removeItem(key)
    }     
    //调用
    setLocalStorage('color','#ffff')
    getLocalStorage('color')
```
<h3>sessionStorage</h3>
sessionStorage 方法针对一个 session 进行数据存储。当用户关闭浏览器窗口后，数据会被删除。
```js
    //  设置 sessionStorage
    function setSessionStorage(key,val){
        return sessionStorage.setItem(key,val)
    } 
    // 获取 sessionStorage
    function getSessionStorage(key){
        return sessionStorage.getItem(key)
    } 
    //删除
    function removeSessionStorage(key){
        return sessionStorage.removeItem(key)
    }     
    //调用
    setSessionStorage('color','#ffff')
    getSessionStorage('color')  
```















