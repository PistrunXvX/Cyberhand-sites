<script>

</script>

<footer class="container-fluid">
    <div class="container footer_container">
        <div class="row justify-content-between footer_all-content">
            <div class="col-8 footer-left_block">
                <p><a href="mailto:contact@cyberhand.ru">contact@cyberhand.ru</a></p>
                <p><a href="tel:+79999027464">+7 (999) 902-74-64</a></p>
                <p>© CyberHand Web Studio 2020</p>
            </div>
            <div class="col-4 social_link  justify-content-center">
                <p>Cyber Hand</p>
                <ul>
                    <li><a href="#">Tg</a></li>
                    <li><a href="#">Vk</a></li>
                    <li><a href="#">In</a></li>
                    <li><a href="#">Fb</a></li>
                </ul>
            </div>
        </div>
    </div>
</footer>
<style lang="scss" >
@import 'style/theme.scss';
@import 'style/resize.scss';

.container-fluid{
   padding-top: 3%;
background-color: $colorYellow;
font-family: $opensans;
font-weight: 700;

}




.footer_all-content{


    p,
    a,
    li{
color:$colorWhite;
text-transform: uppercase;
text-decoration: none;
list-style: none;

    }



}

.footer-left_block{

    a{

        line-height: 92.8%;
        transition: color 0.4s ease-in-out;

    }

    a:hover{
        transition: color 0.4s ease-out;
    color: $darkColor;

    }

    p:first-child a{
        font-size: 46px;
    }

    p:first-child::after{
        margin-top: 2%;
        display: block;
        content: '';
        width: 45%;
        height: 2px;
        background-color: $colorWhite;
    }

    p:nth-of-type(2) a{
        font-size: 43px;
    }
    p:last-child {
        margin-top:6%;
        text-transform: none;
        font-size: 42px;
    }
}

.social_link{
    a{
        transition: color 0.2s ease-in-out;
    }
    p{

        font-size: 52px;
        line-height: 115.3%;
        padding-left: 7.5%;
        margin-bottom: 11%;

    }

    ul{
        display: flex;
        flex-direction: row;
        margin: 0px;
        padding: 0px;
        margin-right: 5%;

    }

    li:not(:last-child){
        margin-right: 20%;
    }

     li a {

        padding: 55%;
        font-size: 25px;
        color: rgba(255, 255, 255, 0);
     }

     li:nth-of-type(1) a{

        background-image: url("/img/soc-icon-teleg.svg");
        background-position: center;
        background-repeat: no-repeat;
        background-size: contain;
        transition: filter 0.5s ease-linear;
     }
     li:hover a{
        transition: filter 0.5s ease-linear;
        filter: opacity(65%);
     }
     li:nth-of-type(2) a{

      background-image: url("/img/soc-icon-vk.svg");
      background-position: center;
      background-repeat: no-repeat;
      background-size: contain;
      transition: filter 0.5s ease-linear;
   }

   li:nth-of-type(3) a{

      background-image: url("/img/soc-icon-inst.svg");
      background-position: center;
      background-repeat: no-repeat;
      background-size: contain;
      transition: filter 0.5s ease-linear;
      padding: 85%;
   }

   li:nth-of-type(4) a{

      background-image: url("/img/soc-icon-fb.svg");
      background-position: center;
      background-repeat: no-repeat;
      background-size: contain;
      transition: filter 0.5s ease-linear;
   }
}



</style>
