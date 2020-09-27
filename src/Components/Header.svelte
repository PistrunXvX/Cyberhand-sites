<script>
    import { link } from "svelte-routing";
</script>

<header class="container-fluid">
    <div class="row">
        <div class="col logo">
            <nav>
                <ul class="nav justify-content-end">
                    <li class="nav-item">
                        <a href="/" use:link>
                            Главная
                        </a>
                    </li>
                    <li class="nav-item">
                        <a href="/portfolio" use:link portfolio>
                            Портфолио
                        </a>
                    </li>
                    <li class="nav-item">
                        <a href="/about_us" use:link about_us>
                            О нас
                        </a>
                    </li>
                    <li class="nav-item">
                        <a href="/price" use:link price>
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
     @import 'style/resize.scss';

     .container-fluid{
         background-color: $darkColor;
     }

    li{
        padding-right: 5%;

        z-index: 1;

        a{
            font-family: $opensans;
            // font-size: 36px;
            font-size: $fontBigP;
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
    }
    .logo{
        padding-top: 3%;
        margin-top: 3%;
		background-image:url("/img/iconLogo.svg");
        background-position: 20%, 50%;
        background-size: contain;
		background-repeat: no-repeat;
    }
 </style>
