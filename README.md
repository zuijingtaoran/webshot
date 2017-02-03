# webshot
@web:
   src="DOC/JS/jquery-1.11.3.js" type="text/javascript"
     src="DOC/layer/layer.js" type="text/javascript"

        $(function () {
            $('.layui-btn').click(function () {
                setTimeout(function () {
                    $('.layui-layer-content,.layui-layer').css('background-color', 'transparent');
                    $('.layui-layer-btn').remove();
                }, 100)
                layer.open({
                    type: 1
  , offset: 'lt' //具体配置参考：offset参数项
 , area: ['400px', '250px']
  , btn: '关闭全部'
  , shade: 0 //不显示遮罩
           });
            })
        });
        function t() {
         v={ t:  $(".layui-layer").offset().top,
           l: $(".layui-layer").offset().left,
           w: $(".layui-layer").css('width'),
           h: $(".layui-layer").css('height')
       }
       console.log(v);
        }
      
@node
var webshot = require('webshot'); var fs = require('fs'); var path = require('path');
var basePath = path.dirname(__filename).replace("routes","")+"/public/18158";  
if (fs.existsSync(basePath)) {  
    console.log('已经创建过此更新目录了');  
} else {  
    fs.mkdirSync(basePath);  
    console.log('更新目录已创建成功\n');  
}  
var options = {
  screenSize: {
    width: 1280
  , height: 768
  }
, shotSize: {
    width: 300
  , height: 400
  }
,shotOffset:{
	
	left:200
	,top:100
}
, userAgent: 'Mozilla/5.0 (iPhone; U; CPU iPhone OS 3_2 like Mac OS X; en-us)'
    + ' AppleWebKit/531.21.20 (KHTML, like Gecko) Mobile/7B298g'
    ,renderDelay:3000
// , cookies: [
//      {
//        name:     'UserName',
//        value:    'user=18158',
//        domain:   'localhost',
//        path:     '/'
//      }
//    ]
      ,onLoadFinished:function() {

}
 
};
//var url='http://finance.ifeng.com/a/20170203/15175396_0.shtml';
//webshot(url,'public/image/sel.png',options, function(err) { 
// 
// err?console.log(err):console.log("ok");
// 
//}); 
@reference
npm isntall  webshot-cli 
https://www.npmjs.com/package/webshot
http://javascript.ruanyifeng.com/tool/phantomjs.html#toc5
