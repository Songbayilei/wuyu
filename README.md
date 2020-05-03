# wuyu
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">

<head>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
    <title>倒计时</title>
    <link rel="stylesheet" href="style.css" />
</head>

<body>
    <div class="time">还剩 <span id="LeftTime"></span></div>
    <script>
    function FreshTime() {
        var endtime = new Date("2017/9/30,18:05:00"); //结束时间
        var nowtime = new Date(); //当前时间
        var lefttime = parseInt((endtime.getTime() - nowtime.getTime()) / 1000);
        d = parseInt(lefttime / 3600 / 24);
        h = parseInt((lefttime / 3600) % 24);
        m = parseInt((lefttime / 60) % 60);
        s = parseInt(lefttime % 60);
        document.getElementById("LeftTime").innerHTML = d + "天" + h + "小时" + m + "分" + s + "秒";
    }
    FreshTime()
    var sh;
    sh = setInterval(FreshTime, 1000);
    </script>
</body>

</html>
