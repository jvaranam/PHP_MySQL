html codeadsfads

    <!DOCTYPE html>
    <html>
    <head>
      <title>AJAX Request</title>
      <script type="text/javascript" src="http://code.jquery.com/jquery-1.9.1.js"></script>
      <script type="text/javascript">
        function chk(){
          var fname=document.getElementById("fname").value;
          var lname=document.getElementById("lname").value;
          var dataString = 'name='+name;

          $.ajax({
            type:"post",
            url:"temp.php",
            data:dataString,
            cache:false,
            success:function(response){
              $("#msg").html(response);
            }
          })
        }
      </script>
    </head>
    <body>
      <form>
        <input type="text" id="fname">
        <input type="text" id="lname">
        <input type="submit" value="submit" onclick="chk()">
      </form>
      <p id="msg"></p>

    </body>
    </html>
