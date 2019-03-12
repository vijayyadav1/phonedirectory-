# phonedirectory-
<html>
    <head>
        <style>
            body
            {
                margin: 0%;
            }
            .header
            {
                width: 100%;
                height: 80px;
                color: white;
                line-height: 80px;
                background-color: black;
                font-size: 25px;
            }
            .container, .enter
            {
                width: 50%;
                height: 50%;
                margin-top: 10%;
                margin-left: 25%;
                border: 1px solid black;
            }
            .enter
            {
                display: none;
            }
            .add, .back
            {
                width: 10%;
                height: 10%;
                margin-left: 8%;
                margin-top: 5%;
                color: white;
                font-size: 20px;
                line-height: 230%;
                position: sticky;
                top: 5%;
                cursor: pointer;
                background-color: #068b18;
            }
            .title
            {
                margin-left: 8%;
                margin-top: 5%;
                margin-bottom: 2%;
                font-size: 20px;
                display: inline-block;
                border: 1px solid black;
                padding: 1%;
            }
            #cono
            {
                margin-left: 21%;
            }
            #name, #contact
            {
                margin-left: 8%;
                margin-top: 5%;
                width: 50%;
                height: 10%;
                padding: 1%;
                font-size: 15px;
            }
            .title:hover
            {
                background-color: black;
                color: white;
            }
            .box
            {
                width: 80%;
                height: 10%;
                margin-top: 1%;
                margin-left: 5%;
            }
            .smalls, .small
            {
                display: inline-block;
                font-size: 20px;
                width: 40%;
                height: 90%;
                line-height: 200%;
                text-transform: uppercase;
                vertical-align: top;
            }
            .small
            {
                width: 30%;
                margin-left: 7%;
            }
            .remove
            {
                display: inline-block;
                width: 11%;
                height: 95%;
                margin-left: 5%;
                margin-top: 1%;
                font-size: 18px;
                background-color: crimson;
                color: white;
                line-height: 150%;
            }
            .new
            {
                width: 80%;
                height: 55%;
                margin-left: 5%;
                overflow-y: scroll;
            }
        </style>
        <script>
            var count = -1;
            var obj = [];
            function add()
            {
                document.getElementById("container").style.display = "none";
                document.getElementById("enter").style.display = "inline-block";
            }
            function back()
            {
                document.getElementById("container").style.display = "inline-block";
                document.getElementById("enter").style.display = "none";   
            }
            function addnew()
            {
               document.getElementById("container").style.display = "inline-block";
               document.getElementById("enter").style.display = "none";
               var a = document.getElementById("name").value;
               var b = document.getElementById("contact").value;
               var z = document.createElement("div");
               z.setAttribute("class", "box");
               z.setAttribute("id", "a"+count);
               var w = document.createElement("div");
               w.setAttribute("class", "smalls");
               w.innerHTML = a;
               z.appendChild(w);
               var v = document.createElement("div");
               v.setAttribute("class", "small");
               v.innerHTML = b;
               z.appendChild(v);
               var u = document.createElement("div");
               u.setAttribute("class", "remove");
               u.setAttribute("id", ""+count);
               u.setAttribute("onclick", "erase(this)");
               u.innerHTML = "Remove";
               z.appendChild(u);
               var y = document.getElementById("new");
               y.appendChild(z);
            }
            function erase(e)
            {
                var did = e.id;
                var elem = document.getElementById("a" + did);
                elem.remove();
            }
        </script>
    </head>
    <body>
        <div class="header"><center>Phone Directory</center></div>
        <div class="container" id="container">
            <div class="add" id="add" onclick="add()"><center>+ Add</center></div>
            <div id="tono" class="title"><center>Name</center></div>
            <div id="cono" class="title"><center>Contact No</center></div>
            <div id="new" class="new">

            </div>
        </div>
        <div class="enter" id="enter">
            <div class="back" onclick="back()"><center>- Back</center></div>
            <input type="text" id="name" placeholder="Name">
            <input type="text" id="contact" placeholder="Contact No">
            <div class="add" onclick="addnew()"><center>Add</center></div>
        </div>
    </body>
</html>
phonebook.html
Displaying phonebook.html.
