<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>age_calculator_by_chandan</title>
</head>
<body>
        <style>
        *{
            margin: 0;
            padding: 0;
            box-sizing: border-box;

        }
        #contanier{
            width: 100%;
            min-height: 100vh;
            background-color: lightslategray;
        }
        #calc{
            width: 800px;
            font-size: 30px;
            color: whitesmoke;
            padding-top: 200px;
            padding-left: 100px;
            /* border-left: black solid 50px;
            border-right: black solid 50px; */

        }
        #date-input{
            width: 500px;
            height: 80px;
            /* margin-right: 0px; */
            padding: 20px;
            border-radius: 10px;
            background-image: linear-gradient(180deg, rgb(174, 165, 184), rgb(132, 130, 134));
            display: flex;
            align-items: center;
            /* justify-content: space-around; */
             /* border-left: black solid 50px;
            border-right: black solid 50px; */
        }
        #date-input input{
            flex: 1;
            margin-right: 20px;
            padding: 14px 20px;
            border: 0;
            outline: 0;
            font-size: 17px;
            border-radius: 5px;
            position: relative;
        }
        #date-input button{
            border: 0;
            outline: 0;
            font-size: 20px;
            border-radius: 50%;
            padding: 20px;
            background-image: linear-gradient(to right, rgba(255,0,0,0), rgb(236, 199, 199));

        }
        span{
            color:rgb(76, 10, 228);
        }
        p{
            color: white;
            
        }
    </style>
    <body>
        <div id="contanier">
            <div id="calc">
             <h1>Here you can <br><span>Calculate your age</h1></span>
             
                <div id="date-input">
                    <input type="date" id="date">
                    <button> Calculate </button>
                </div>
             
                <p id="result"></p>   
            </div>
            
        </div>
        
    </body>
        </html>
</body>
</html>
<script>
    
        let inp = document.querySelector("input");
        let btn = document.querySelector("button");
        let p = document.getElementById("result")

        btn.onclick = () => {

        
            let year1 = Number(inp.value.split("-")[0]);
            let month1 = Number(inp.value.split("-")[1]);
            let date1 = Number(inp.value.split("-")[2]);


            let date = new Date();

            let date2 = date.getDate()
            let year2 = date.getFullYear();
            let month2 = date.getMonth() + 1;

            let x = year2 - year1;
            let y = month2 - month1;
            let z = date2 - date1;
            p.innerHTML = "You" + " " + "are" + " " + x + " " + "years" + " " + y + " " + "months" + " " + "and" + " " + z + " " + "days old"
        }
</script>
