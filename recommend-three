/// <reference path="../../javascript/js基础/scripts/jquery-1.10.2.js" />

/**
  不知道为什么页面加载完成时还读不到div_digg。可能也是动态生成的。
  所以这里只能用定时器 不断的读取，当读取到了再给它动态添加快捷按钮
**/

//自定义 定时器[当元素加载完成是执行回调函数]
function customTimer(inpId,fn) {
    if ($(inpId).length) {
        fn(); 
    }
    else {
        var intervalId = setInterval(function () {
            if ($(inpId).length) {  //如果存在了
                clearInterval(intervalId);  // 则关闭定时器
                customTimer(inpId,fn);              //执行自身
            }
        }, 100);
    }
}

//页面加载完成是执行
$(function () {
    customTimer("#div_digg", function () {
        var div_html = "<div class=''>\
                        <a href='javascript:void(0);' onclick='c_follow();'>关注</a>\
                         &nbsp;|&nbsp;\
                        <a href='#top'>顶部</a>\
                         &nbsp;|&nbsp;\
                        <a href='javascript:void(0);' onclick=\" $('#tbCommentBody').focus();\">评论</a>\
                   </div>";
        $("#div_digg").append(div_html);
        //tbCommentBody    
    });
});


//$("body,html").animate({ scrollTop: 0 }, 150);
