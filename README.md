# webstroge



这里主要讨论一下几种web存储方式

<h3>cookie</h3>
特点：

每次http请求头都会携带

大小小于4k

设置cookie的方法

//在本地可以用火狐浏览器测试<br>

//this example should be running in a server condition

cookie的存储形式
```
arrial=1; wocap=nima
```
具体设置方法参见cookie.html

<h3>localstorage</h3>

localStorage 方法存储的数据没有时间限制，除非手动删除

每个域名能存储5M数据

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
    localStorage.key(0)//取出第一条数据的key
    //删除
    function removeLocalStorage(key){
        return localStorage.removeItem(key)
    }  
    localStorage.clear()//删除所有
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
<a href="http://www.jb51.net/html5/144597.html">参考链接</a>

<h3>indecDB</h3>
<a href="http://javascript.ruanyifeng.com/bom/indexeddb.html">参考链接</a>














