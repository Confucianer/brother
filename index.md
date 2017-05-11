<html xmlns="http://www.w3.org/1999/xhtml">  
    <head>  
        <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />  
        <title>New Web Project</title>  
        <script type="text/javascript">  
          
            var timer = null;  
            var width = 0;  
            function doStart() {  
                timer =setTimeout("onChange()", 10);  
            }  
  
            function doStop() {  
                clearTimeout(timer);  
            }  
  
            function onChange() {  
                if(width == 400) {  
                    clearTimeout(timer);  
                }else {  
                    width += 1;  
                    document.getElementById("div2").style.width = width + "px";
                    var id = document.getElementById('num');
                    id.innerHTML = parseInt(width/4);  
                    // document.write(parseInt(width/4));
                    timer = setTimeout("onChange()", 10);  
                }  
            }  
  
        </script>  
    </head>  
    <body>  
        <div style="height: 20px;width: 400px;border: 1px solid gray;padding: 2px">  
            <div style="height:20px;width:0px;background-color: orange" id="div2">  
            </div>  
            <div id="num">0</div>
        </div>  
        <br />  
        <input type="button" value="开始" onclick="doStart()" />  
        <input type="button" value="停止" onclick="doStop()" />  
    </body>  
</html>  
