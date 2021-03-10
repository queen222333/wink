# wink
 // 简介： 正则表达式   用于判定字符串是否符合正确规则
        /* 
            定义正则表达式； 
                1  var reg = /pattern/igm;
                2  var reg = new RegExp("pattern", "igm");
         */
        /* 
            正则表达式中的元字符:
                \s  表示所有的空白符
                \S  表示所有的非空白符
                \w  所有的数字、字母、下划线
                \W  所有的非(数字、字母、下划线)
                \d  所有的数字
                \D  所有的非数字
            正则表达式中的特殊字符：
                ^ 表示开头
                $ 表示结尾
                () 表示分组  也能用$1表示（）里的数据！！
                [] 表示范围
                {} 表示数量
                ? 表示数量 1个或0个
                + 最少1个最多不限制
                * 最少0个最多不限制
                | 或者
                . 除了回车和换行之外的任意字符
            
         */
        // // 有一个字符 检测它是否是abcde中的任意一个
        // var str= "a";
        // var reg = /[abcde]/;
        // var result = reg.test(str);
        // console.log(result);
        //  var str='a';
        //  var reg=/[abcde]/
        //  console.log(reg.test(str));
        // // 随机生成一个字符 检测它是否是abcde中的任意一个
        // var arr = "abcdefghijklmnopqrstuvwxyz".split('');
        // var str= arr[parseInt(Math.random() * arr.length)]
        // var reg = /[abcde]/;
        // var result = reg.test(str); 
        // console.log(result)
          var arr='ahdidhjsjskfnjsdnf'.split('');//用空字符切割成数组
          var str=arr[parseInt(Math.random()*arr.length)];//取任意一个字符
          var reg=/[abcde]/;
          console.log(reg.test(str))
        // 检测一个字符串中是否包含hello world
        // var str = "beijing hello world guangzhou";
        // var reg = /hello world/;
        // console.log(reg.test(str));
        
        
        
        
        // 检测一个字符串是否是以beijing开头
        var str = "   beijing hello world guangzhou";
        // var str1 = str.trim(); 
        // var reg = /^\s*beijing/;
        // console.log(reg.test(str));
        // console.log(reg.test(str1));
        var str1=str.trim(); //清除字符串两边的空白
        var reg=/^\s*beijing/;
        console.log(reg.test(str))
        console.log(reg.test(str1))

        // 检测是否是手机号
        var tel = "15367980655";
        // var reg = /^1\d{10}$/; // 如果去掉^ 和 $ 则只要tel中包含符合该规则的字符串就为真
        // console.log(reg.test(tel));
         var reg=/^1\d{10}$/
         console.log(reg.test(tel));

        // 检测是否是邮箱
        var email = "993155435@qq.com";
        // var email_reg = /^\w{1,12}@\w{1,8}\.(com|cn|top|org)$/;
        // console.log(email_reg.test(email));
        var reg=/^\w{1,12}@\w{1,8}\.(com|cn|top|org)$/;
        console.log(reg.test(email));
        // 汉字 需要使用unicode编码
        var reg = /[\u4e00-\u9fa5]{3}/;
        var str = "大帅哥";
        console.log(reg.test(str));
