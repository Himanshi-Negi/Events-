# Events-
This is my first repository that shows how the color of the webpage changes.
//HTML:-
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8"/>
        <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
        <title>DOCUMENT2</title>
        <link rel="stylesheet" href="style.css"/>
    </head>

    <body class="abc">
        <div class="box">1st box</div>
        
        <script src="Events.js"></script>
    </body>
</html>

//CSS:-
.box{
    height:100px;
    background-color: aqua;
    color:black;
}
.newbox{
    height:100px;
    background-color: black;
    color:aqua;
}
.abc{
    background-color: bisque;
}
.xyz{
    background-color: burlywood;
}

//JAVASCRIPT:-
let div=document.querySelector(".box");
let body=document.querySelector("body");
let class1 ="box" ;
div.addEventListener("mouseover",()=>
{
    if (class1==="box")
    {
        class1="newbox";
        div.classList.add("newbox");
        div.classList.remove("box");
        body.classList.add("xyz");
        body.classList.remove("abc");
    }
    else
    {
        class1="box";
        div.classList.add("box");
        div.classList.remove("newbox");
        body.classList.add("abc");
        body.classList.remove("xyz");
    }
    
})
