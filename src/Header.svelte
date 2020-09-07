<header class="container-fluid">
    <div class="row">
        <div class="col logo">
            <nav>
                <ul class="nav justify-content-end">
                    <li class="nav-item">
                        <a href="#">
                            Главная
                        </a>
                    </li>
                    <li class="nav-item">
                        <a href="#">
                            Портфолио
                        </a>
                    </li>
                    <li class="nav-item">
                        <a href="#">
                            О нас
                        </a>
                    </li>
                    <li class="nav-item">
                        <a href="#">
                            Услуги
                        </a>
                    </li>
                </ul>
            </nav>
        </div>
    </div>
</header>

 <style lang="scss">
     @import 'style/theme.scss';

    li{
        padding-right: 5%;
        
        z-index: 1;

        a{
            font-family: $opensans;
            font-size: 36px;
            text-decoration: none;

            color: $colorWhite;
            line-height: 1;
            display: inline-block;
        }
        a:after {
            display: block;
            content: "";
            height: 2px;
            width: 0%;
            background-color: $dark-orange;
            transition: width .3s ease-in-out;
        }
        a:hover:after,
        a:focus:after {
            width: 100%;
        }
            // a:hover,
            // a:focus {
            //     color: $colorGray;
            // }
        
    }
    .logo{
        padding-top: 3%;
        margin-top: 3%;
		background-image:url("/img/iconLogo.svg");
        background-position: 20%, 50%;
        background-size: contain;
		background-repeat: no-repeat;
    }


    

//      .container-fluid{
//          display: flex;
//          justify-content: flex-end;
//      }


//     .nav{
//       padding-top: 5px;
//       margin-right: 68px;
//     }
//         .nav li  {
//          position: relative;
//         }

//         .nav li a::before{
//             content:'';
//             position: absolute;
//             display: inline-block;
//             width: 85%;
//             height: 2px;
//             background-color: $dark-orange;
//             margin-top: 50px;   
            
//         }

//     .nav > li > a{
//    color:white;
//    font-family: $opensans;
//    font-size: 36px;
//     }

    
//     .nav li:not(:last-child) {
//         margin-right: 70px;
//     }

 </style>