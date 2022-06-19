# aldo-resolusi
untuk menyimpan rencana ke-depan

(HTML)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>wTC.</title> 
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="menu">
        <li class="item" id="mn1">
            <a class="btn" href="#mn1">Users</a>
            <div class="submenu">
                <a href="#">Users list</a>
                <a href="#">add User</a>
                <a href="#">delete User</a>
            </div>
        </li>
        <li class="item" id="mn2">
            <a class="btn" href="#mn2">Files</a>
            <div class="submenu">
                <a href="#">Users list</a>
                <a href="#">add File</a>
                <a href="#">delet file</a>
            </div>
        </li>
    </div>
    <div class="animated-background"></div>
</body>
  
  (CSS)
  .menu{
width: 300px;
height: auto;
background: #162447;
border-radius: 8px;
overflow: hidden;
box-shadow: 0 0 10px rgba(0, 0, 0, -5);
}

.menu .btn{
    display: block;
    padding: 1rem;
    border-bottom: solid 1px #1b1b2f;
    border-top: solid 1px #1f4068;
    position: relative;
}

.menu .submenu{
    background: #1b1b2f;
    overflow: hidden;
    max-height: 0;
    transition: max-height .8s ease-out;
}

.menu .submenu a{
    display: block;
    padding: 1rem;
    position: relative;
}

.menu .submenu a::before{
    content: '';
    display: block;
    position: absolute;
    top: o;
    left: 0;
    height: 180%;
    width: 5px;
    background: #e43f5a;
    opacity: 0;
    transition: all .5s;
}

.menu .submenu a:hover{
    padding-left: calc(1rem + 5px);
    opacity: 1;
}

.item:target .submenu{
    max-height: 20rem;
}

.animated-background{
    background: linear-gradient(
        to rigth, #833ab4,
        #fd1d1d, #fcb045);
        background-size: 400% 400%;
        animation: animate-background 10s infinite ease-in-out;

        @keyframes animated-background {
            0%{
        background-position: 0 50%;
            }
            50%{
        background-position: 100% 50%;
            }
            100%{
        background-position:  0 50%;
            }
        
        }
    }
