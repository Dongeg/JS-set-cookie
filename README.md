# set-cookie
设置cookie的方法
//需要在服务器环境下才能起作用<br>
//this example should be running in a server condition
```html
      <!DOCTYPE html>
      <html>
      <head>
      <meta charset="utf-8">
      <title>cookie应用</title>
      <style>
      #div1 {
        width:200px; 
        height:200px; 
        background:#CCC; 
        display:none;
      }
      </style>
      <script>
      /* 如果没有cookie信息，将显示div，否则不显示。 （请在火狐浏览器下测试） */
      //设置cookie
      function setCookie(name, value, iDay){
          var oDate=new Date();
          oDate.setDate(oDate.getDate()+iDay);
          document.cookie=name+'='+value+';expires='+oDate;    
      }
      
      //读取cookie
      function getCookie(name)
      {
        var arr=document.cookie.split(';');  //定义一个数组
        var re=new RegExp('\\b'+name+'=\\w+');  //定义一个正则
        var res=document.cookie.match(re);  //匹配所选字段
        if(res){
          return res[0].split('=')[1]; //如果匹配成功，返回结果
        }
        else
        {
          return ''; //否则返回空
        }
      }
      
      //删除cookie
      function removeCookie(name){setCookie(name, '1', -1) } //利用setCookie函数，将时间设置为-1，达到删除效果（默认没有删除方法）
      
      window.onload=function ()
      {
          var oDiv=document.getElementById('div1');
        
        if(!getCookie('arrial'))
        {
          oDiv.style.display='block';
          setCookie('arrial', '1', 30);    //向cookie中添加'arrial', '1', 30
        }
      };
      </script>
      </head>
      
      <body>
      <div id="div1">没有cookie信息</div>
      </body>
      </html>
```
