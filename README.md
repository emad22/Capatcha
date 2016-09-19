     <html>
         <head>
             <script type="text/javascript">
                 function Captcha(){
                     var alpha = new Array('A','B','C','D','E','F','G','H','I','J','K','L','M','N','O','P','Q','R','S','T','U','V','W','X','Y','Z','a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t','u','v','w','x','y','z','1','2','3','4','5','6','7','8','9','0');
                     var i;
                     for (i=0;i<4;i++){
                       var a = alpha[Math.floor(Math.random() * alpha.length)];
                       var b = alpha[Math.floor(Math.random() * alpha.length)];
                       var c = alpha[Math.floor(Math.random() * alpha.length)];
                       var d = alpha[Math.floor(Math.random() * alpha.length)];
                      }
                    var code = a+b+c+d;
                    document.getElementById("mainCaptcha").value = code
                  }
                  function ValidCaptcha(){
                      var string1 = document.getElementById('mainCaptcha').value;
                      var string2 = document.getElementById('txtInput').value;
                      if (string1 == string2){
                         alert("Done");
                      }else if(string2==null || string2==""){
							alert("You Must Enter the character Above");
					  }
                      else{        
                         alert("Try agian !");
                      }
                  }
             </script>    
        </head>
     <body onload="Captcha();">
        <table>
          <tr>
           <td>
             <input type="text" id="mainCaptcha"/>
           </td>
          </tr>
          <tr>
           <td>
            <input type="text" id="txtInput"/>    
          </td>
         </tr>
         <tr>
          <td>
            <input id="Button1" type="button" value="Check" onclick="ValidCaptcha();"/>
          </td>
        </tr>
      </table>
    </body>
 </html>
