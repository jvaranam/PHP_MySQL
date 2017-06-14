Ajax request of type json

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
