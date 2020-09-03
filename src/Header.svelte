<header class="container-fluid">

    <nav>
        <ul class="nav justify-content-end">
            <li class="nav-item">
                <a href="#" class="nav-link">
                    Главная
                </a>
            </li>
            <li class="nav-item">
                <a href="#" class="nav-link">
                    Портфолио
                </a>
            </li>
            <li class="nav-item">
                <a href="#" class="nav-link">
                    О нас
                </a>
            </li>
            <li class="nav-item">
                <a href="#" class="nav-link">
                    Услуги
                </a>
            </li>
        </ul>
    </nav>
</header>

 <style lang="scss">
     @import 'style/theme.scss';

     .container-fluid{
         display: flex;
         justify-content: flex-end;
     }


    .nav{
      padding-top: 5px;
      margin-right: 68px;
    }
        .nav li  {
         position: relative;
        }

        .nav li a::before{
            content:'';
            position: absolute;
            display: inline-block;
            width: 85%;
            height: 2px;
            background-color: $dark-orange;
            margin-top: 50px;   
            
        }

    .nav > li > a{
   color:white;
   font-family: $opensans;
   font-size: 36px;
    }

    
    .nav li:not(:last-child) {
        margin-right: 70px;
    }

 </style>