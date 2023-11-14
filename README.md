# My-Internship-Project3
<!DOCTYPE html>
<html>
<head>
    <script src="https://kit.fontawesome.com/e8fa2e31b4.js" crossorigin="anonymous"></script>
    <style>
        *{
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'poppins', sans-serif;
        }
        body{
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }
        .top-bar{
            width: 80%;
            height: 4rem;
            background-color: #eee;
            margin-bottom: 20px;
            display: flex;
            padding: 0px 20px;
            align-items: center;
            justify-content: space-between;
        }
        .fa-solid{
            color: red;
            margin-right: 10px;
        }
        .header{
            width: 80%;
            height: 200px;
            background-color: red;
            margin-bottom: 20px;
            padding: 20px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }
        .navbar{
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .navbar p{
            font-size: 30px;
            font-weight: bold;
            color: white;
        }
        .navbar ul{
            display: flex;
            list-style: none;
        }
        .navbar ul li a{
            text-decoration: none;
            font-size: 18px;
            color: white;
            padding: 7px 15px;
        }
        .navbar ul li a:hover{
            background-color: white;
            color: red;
            border-radius: 3px;
        }
        .navbar-b{
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
        .dropdown{
            width: 130px;
            text-align: center;
            background-color: white;
            border-radius: 3px;
        }
        select{
            outline: none;
            border: none;
            background: none;
            padding: 7px 10px 7px 0px;
            color: red;
            font-size: 18px;
            cursor: pointer;
        }
        select:hover{
            color: #333;
        }
        .search{
            width: 500px;
            background-color: white;
            height: 45px;
            border-radius: 45px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 15px;
        }
        .search input{
            width: 440px;
            border: none;
            outline: none;
            height: 40px;
        }
        .cart{
            display: flex;
            background-color: white;
            justify-content: space-between;
            align-items: center;
            padding: 7px 10px;
            border-radius: 3px;
            width: 80px;
            font-size: 18px;
        }
        .cart p{
            height: 22px;
            width: 22px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 22px;
            background-color: red;
            color: white;
        }
        .container{
            width: 80%;
            display: flex;
            margin-bottom: 20px;
        }
        #root{
            width: 70%;
            display: grid;
            grid-template-columns: repeat(2, 1fr) ;
            grid-gap: 20px;
        }
        .sidebar{
            width: 30%;
            border-radius: 5px;
            background-color: #eee;
            margin-left: 20px;
            padding: 20px;
            text-align: center;
        }
        .box{
            display: flex;
            justify-content: space-between;
            padding: 20px;
            border: 1px solid #aaa;
            border-radius: 5px;
        }
        .img-box{
            width: 50%;
            height: 170px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .left{
            width: 50%;
            text-align: right;
            display: flex;
            flex-direction: column;
            justify-content: space-evenly;
            margin-left: 60px;
        }
        img{
            max-height: 90%;
            max-width: 90%;
            object-fit: cover;
            object-position: center;
        }
        button{
            border: none;
            border-radius: 5px;
            background-color: red;
            padding: 10px 25px;
            cursor: pointer;
            color: white;
        }
        button:hover{
            background-color: #333;
        }
    </style>
</head>
<body>
    <dic class="top-bar">
        <p><i class="fa-solid fa-envelope"></i>ezlearnaxis@gmail.com</p>
        <p><i class="fa-solid fa-phone"></i>+923180000008</p>
    </dic>
    <div class="header">
        <div class="navbar">
            <p>LOGO</p>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">Store</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </div>
        <div class="navbar-b">
            <div class="dropdown">
                <select name="">
                    <option value="1">Categories</option>
                    <option value="2">New</option>
                    <option value="3">Imported</option>
                    <option value="4">Local</option>
                </select>
            </div>
            <div class="search">
                <input type="search" placeholder="Search...">
                <i class="fa-solid fa-magnifying-glass"></i>
            </div>
            <dic class="cart"><i class="fa-solid fa-cart-shopping"></i><p>0</p></dic>
        </div>
    </div>
    <div class="container">
        <div id="root"></div>
        <div class="sidebar">sidebar</div>
    </div>
    <script>
        const product = [
            {
                id: 1,
                image: 'image/aa-1.jpg',
                title: 'Headphones',
                price: '$20'
            },
            {
                id: 2,
                image: 'image/bb-1.jpg',
                title: 'Rode NT1 Microphone',
                price: '$45'
            },
            {
                id: 3,
                image: 'image/cc-1.jpg',
                title: 'Smart Watch',
                price: '$60'
            },
            {
                id: 4,
                image: 'image/dd-1.jpg',
                title: 'HP Laptop Next Generation',
                price: '$30'
            },
            {
                id: 5,
                image: 'image/ee-1.jpg',
                title: '250D DSLR Camera',
                price: '$65'
            },
            {
                id: 6,
                image: 'image/ff-1.jpg',
                title: 'Metal Dask Lamp',
                price: '$35'
            },
            {
                id: 7,
                image: 'image/gg-1.jpg',
                title: 'Z Flip Foldable Mobile',
                price: '$55'
            },
            {
                id: 8,
                image: 'image/hh-1.jpg',
                title: 'Ari Pods Pro',
                price: '$50'
            },
        ]
        const categories = [...new Set(product.map((item)=>
       {return item}))]

       let img = document.getElementById('root')
       img.innerHTML = categories.map((item)=>
       {
        var {image, title, price} = item;
           return(
           `<div class="box">
                <div class="img-box">
                    <img src=${image}></img>
                </div>
                <div class="left">
                    <p>${title}</p>
                    <h2>${price}</h2>
                    <button>Add to Cart</button>    
                </div>
            </div>`)
       }).join('')
       </script>
</body>
</html>
