<template>
    <header id="header">
        <div class="header-middle">
            <div class="container">
                <div class="row">
                    <div class="col-sm-4">
                        <div class="logo pull-left">Optovka.kz</div>
                    </div>
                    <div class="col-sm-8 text-center">
                        <div class="shop-menu">
                            <ul class="nav navbar-nav">
                                <li><a href="#"><font-awesome-icon class="icon" icon="user" /> Account</a></li>
                                <li><a href="#"><font-awesome-icon class="icon" icon="star" /> Wishlist</a></li>
                                <li><a href="#"><font-awesome-icon class="icon" icon="shopping-cart" /> Cart</a></li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="header-bottom">
            <div class="container">
                <div class="row">
                    <div class="col-sm-3">
                        <div class="search_box pull_right">
                            <input type="text" placeholder="Search" />
                        </div>
                    </div>
                    <div class="col-sm-9">
                        <div class="mainmenu pull-left">
                            <ul class="nav navbar-nav">
                                <li><a href="#" class="active">Home</a></li>
                                <li class="dropdown">
                                    <a href="#">Shop <font-awesome-icon class="fa-angle-down" icon="angle-down" /></a>
                                    <ul role="menu" class="sub-menu">
                                        <li><a href="#">Products</a></li>
										<li><a href="#">Product Details</a></li> 
										<li><a href="#">Checkout</a></li> 
										<li><a href="#">Cart</a></li> 
										<li><a href="#">Login</a></li>
                                    </ul>
                                </li>
                                <li class="dropdown">
                                    <a href="#">Blog <font-awesome-icon class="fa-angle-down" icon="angle-down" /></a>
                                    <ul role="menu" class="sub-menu">
                                        <li><a href="#">Blog List</a></li>
										<li><a href="#">Blog Single</a></li>
                                    </ul>
                                </li>
                                <li><a href="#">404</a></li>
                                <li><a href="#">Contact</a></li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>

<style scoped>
    .icon {
        margin-right: 5px;
    }
    .navbar-nav {
        flex-direction: row;
    }
    .header-middle .container .row {
        border-bottom: 1px solid #f5f5f5;
        margin-left: 0;
        margin-right: 0;
        padding-bottom: 20px;
        padding-top: 20px;
    }
    .shop-menu ul li {
        display: inline-block;
        padding-left: 15px;
        padding-right: 15px;
    }

    .shop-menu ul li:last-child {
        padding-right: 0;
    }


    .shop-menu ul li a {
        background: #FFFFFF;
        color: #696763;
        font-family: 'Roboto', sans-serif;
        font-size: 14px;
        font-weight: 300;
        padding:0;
        padding-right: 0;
        margin-top: 10px;
    }

    .shop-menu ul li a i{
        margin-right:3px;
    }

    .shop-menu ul li a:hover {
        color:#fe980f;
        background:#fff;
    }


    .header-bottom {
        padding-bottom: 30px;
        padding-top: 30px;
    }

    .nav.navbar-nav > li:hover > ul.sub-menu{
        display: block;
        -webkit-animation: fadeInUp 400ms;
        -moz-animation: fadeInUp 400ms;
        -ms-animation: fadeInUp 400ms;
        -o-animation: fadeInUp 400ms;
        animation: fadeInUp 400ms;
    }
    .mainmenu ul li{
        padding-right: 15px;
        padding-left: 15px;
    }

    .mainmenu ul li:first-child{
        padding-left: 0px;
    }

    .mainmenu ul li a {
        color: #696763;
        font-family: 'Roboto', sans-serif;
        font-size: 17px;
        font-weight: 300;
        padding: 0;
        padding-bottom: 10px;
    }

    .mainmenu ul li a:hover, .mainmenu ul li a.active,  .shop-menu ul li a.active{
        background:none;
        color:#fdb45e;
    }

    .search_box input {
        background: #F0F0E9;
        border: medium none;
        color: #B2B2B2;
        font-family: 'roboto';
        font-size: 12px;
        font-weight: 300;
        height: 35px;
        outline: medium none;
        padding-left: 10px;
        width: 155px;
        background-repeat: no-repeat;
        background-position: 130px;
    }
    /*  Dropdown menu*/

    .navbar-header 
    .navbar-toggle .icon-bar {
        background-color: #fff;
    }


    .nav.navbar-nav > li:hover > ul.sub-menu{
        display: block;
        -webkit-animation: fadeInUp 400ms;
        -moz-animation: fadeInUp 400ms;
        -ms-animation: fadeInUp 400ms;
        -o-animation: fadeInUp 400ms;
        animation: fadeInUp 400ms;
    }

    ul.sub-menu {
        position: absolute;
        top: 30px;
        left: 0;
        background: rgba(0, 0, 0, 0.6);
        list-style: none;
        padding: 0;
        margin: 0;
        width: 220px;
        -webkit-box-shadow: 0 3px 3px rgba(0, 0, 0, 0.1);
        box-shadow: 0 3px 3px rgba(0, 0, 0, 0.1);
        display: none;
        z-index: 999;
    }

    .dropdown ul.sub-menu li .active{
        color: #FDB45E;
        padding-left: 0;
    }


    .navbar-nav li ul.sub-menu li{
        padding: 10px 20px 0 ;
    }

    .navbar-nav li ul.sub-menu li:last-child{
        padding-bottom: 20px;
    }

    .navbar-nav li ul.sub-menu li a{
        color: #fff;
    }

    .navbar-nav li ul.sub-menu li a:hover{
        color: #FDB45E;
    }

    .fa-angle-down{
        padding-left: 5px; 
    }

    @-webkit-keyframes fadeInUp {
        0% {
            opacity: 0;
            -webkit-transform: translateY(20px);
            transform: translateY(20px);
        }

        100% {
            opacity: 1;
            -webkit-transform: translateY(0);
            transform: translateY(0);
        }
    }
</style>