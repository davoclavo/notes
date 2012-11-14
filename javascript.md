Javascript Notes
================

#Document ready

Good

    $(function(){
        ...
    });

    $(document).ready(function(){
        ...
    });

Bad

    $().ready(function(){
        ...
    });

#jQuery variables

Good

    $bar = $(bar);

Bad

    bar = $(bar);