Ajax request of type json  - html code

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
                url: '[url]',
                type: "POST",
                dataType: "json",
                data: { [ action_type: 'create', data: { tableName: projectName }, id: 10 ] },
                success: function(data) {
                  onSuccessCall(data)
                }.bind(this),
                error: function(data) {
                    onErrorCall(data);
                }.bind(this)
            });
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
    
PHP Code 
 
    <?php 
        $action = $_POST['action'];
        $data = $_POST['data'];

        echo "Action : ".$action. "<br/>Table name : ".$data[tableName];
    ?>

