<script>

</script>
<div class="container-fluid">
    <section class="container-fluid first__container">
        <div class="row">
            <h1>О нас</h1>
            <div class="col-xl-12">
                <div class="about_block">

                    <div class="about_slider">

                        <div id="carouselExampleInterval" class="carousel slide" data-ride="carousel">
                            <div class="carousel-inner">
                                <div class="carousel-item active" data-interval="2000">
                                    <img src="/img/loshariki.jpg" class="d-block w-100" alt="">
                                </div>
                                <div class="carousel-item">
                                    <img src="/img/loshariki.jpg" class="d-block w-100" alt="">
                                </div>
                            </div>
                            <a class="carousel-control-prev" href="#carouselExampleInterval" role="button"
                                data-slide="prev">
                                <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                                <span class="sr-only">Previous</span>
                            </a>
                            <a class="carousel-control-next" href="#carouselExampleInterval" role="button"
                                data-slide="next">
                                <span class="carousel-control-next-icon" aria-hidden="true"></span>
                                <span class="sr-only">Next</span>
                            </a>
                        </div>

                    </div>
                </div>

            </div>
        </div>

    </section>

    <section class="container-fluid second__container ">

        <div class="row">
            <h3 class="second__title">Мы команда с одним интересом!</h3>
            <div class="col-xl-6 col-lg-6 col-md-12 col-sm-12 col-xs-12">
                
                    <div class="card__item ">
                        
                        <div class="card__item_image">

                            <img src="/img/card.jpg" alt="" class="img-fluid">
                        </div>
                        <a href=""></a>
                        <div class="card__item_text">
                            <h3>Шершнёв Артём</h3>
                            <p>Веб - дизайнер.</p>
                        </div>
                    </div>

                </div>

                <div class="col-xl-6 col-lg-6 col-md-12 col-sm-12 col-xs-12">

                    <div class="card__item">
                        <div class="card__item_image">

                            <img src="/img/card.jpg" alt="" class="img-fluid">
                        </div>

                        <div class="card__item_text">
                            <h3>Евгений Горячкин</h3>
                            <p>Фронтенд - разработчик.</p>
                        </div>
                    </div>

                </div>




                <div class="row ">

                    <div class="col-xl-6 col-lg-6 col-md-12 col-sm-12 col-xs-12">
                        <div class="card__item">
                            <div class="card__item_image">

                                <img src="/img/card.jpg" alt="" class="img-fluid">
                            </div>

                            <div class="card__item_text">
                                <h3>Лебедев Александр</h3>
                                <p>Фронтенд - разработчик.</p>
                            </div>
                        </div>

                    </div>

                    <div class="col-xl-6 col-lg-6 col-md-12 col-sm-12 col-xs-12">

                        <div class="card__item">
                            <div class="card__item_image">

                                <img src="/img/card.jpg" alt="" class="img-fluid">
                            </div>

                            <div class="card__item_text">
                                <h3>Валерия Княгинина</h3>
                                <p>SMM - специалист.</p>
                            </div>
                        </div>

                    </div>

                </div>

            </div>


    </section>

</div>
<style lang="scss">
    @import "style/theme.scss";
    @import "style/resize.scss";




    .first__container {
        padding-top: 10%;

        background-image: url("/img/bubble.png");
        background-position: top right;
        background-repeat: no-repeat;
        background-size: 50%;
        
        h1 {
            text-transform: uppercase;
            font-weight: 700;
            padding-left: 6%;
            font-size: 153px;
            padding-bottom: 6%;
            line-height: 115.3%
        }
    }

    .container-fluid {
        padding-left: 3%;
        padding-right: 3%;
        background-color: $darkColor;
        color: $colorWhite;
        font-family: $opensans;
    }


    .second__container {
        padding-bottom: 15%;

        background-image: url("/img/bubble.png");
        background-position: bottom left;
        background-repeat: no-repeat;
        background-size: 30%;

        .card__item_text{
            padding-top: 2%;
        }

        .second__title {
            
            text-align: center;
            padding-top: 5%;
            padding-bottom: 5%;
            font-size: 46px;
            line-height: 115.3%;
        }

        h3{
            font-size: 46px;
            font-weight: 700;
            line-height: 115.3%;
        }

        p{
            font-style: italic;
            font-weight: 100;
            font-size: 34px;
        }
       

    .card__item{
        padding-bottom: 20%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        
    }


    .card__item{
        padding-bottom: 20%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        
    }

}

 //animation

 .card__item{
        transition:all 0.3s ease-out;
    }

    .card__item:after{
        display: block;
     content: "";
     width: 0%;
     height: 11px;
     background-color:$dark-orange ;
     transition: width .3s ease-in-out;
    }

    .card__item:hover:after,
    .card__item:focus:after{
        transition: width .3s ease-in-out;
        width: 100%;
    }

    .card__item:hover{
        transition:all 0.3s ease-out;
        box-shadow: 10px  10px 24px black;
        color:#b5026d;
        
    }

    


    


   
    


</style>