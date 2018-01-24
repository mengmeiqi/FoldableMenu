# FoldableMenu
    折叠菜单
#### 找到该元素的兄弟（元素节点）
         function next(elem){
             do{
                 elem = elem.nextSibling;
             }while(elem && elem.nodeType != 1);
             return elem;
         }
#### 找到该元素的第一个孩子（元素节点）
         function first(elem){
             elem = elem.firstChild;
             return elem.nodeType ==1 ? elem : next(elem);
         }
#### $(this).next().stop(false,true).slideToggle(1000);
        .next() 元素紧邻的后面同辈元素的元素
        .stop() 停止匹配元素当前正在运行的动画。
            两个参数 .stop(clearQueue,jumpToEnd)
            clearQueue 一个布尔值，指示是否取消以列队动画，默认false
            jumpToEnd 一个布尔值，指示是否当前动画立即完成，默认false
        .slideToggle(time) 用滑动动画显示或隐藏一个匹配元素