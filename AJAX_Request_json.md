Ajax request of type json  - html code

    <!DOCTYPE html>
    <html>
    <head>
      <title>AJAX Request</title>
      <script type="text/javascript" src="http://code.jquery.com/jquery-1.9.1.js"></script>
      <script type="text/javascript">
        function chk(){
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
      <h3> ajax json call </h3>
    </body>
    </html>
    
PHP Code 
 
    <?php 
        $action = $_POST['action'];
        $data = $_POST['data'];

        echo "Action : ".$action. "<br/>Table name : ".$data[tableName];
    ?>

