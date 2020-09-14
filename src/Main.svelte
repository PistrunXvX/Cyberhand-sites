<script>

</script>

<main class="container-fluid">
    <section class="container first__container">
        <div class="row">
            <div class="col-8">
                <div class="main_text">
                    <h1>Cyber Hand</h1>
                    <h3>Ваш сайт - наша работа</h3>
                    <p>
                        Создаем интерфейсы аналитических систем, мобильные приложения и цифровые сервисы для государства и крупного бизнеса
                    </p>
                    <button type="button" class="btn first__button">Свяжитесь с нами</button>
                </div>
            </div>
            <div class="col-4 video_block">
                <video src="#"></video>
            </div>
        </div>
    </section>
    <section class="container second__container">
        <div class="row">
            <div class="col">
                <div class="about_text">
                    <h2>О нашей студии</h2>
                    <p>
                        Мы - небольшая веб-студия и группа единомышленников. Специализируемся на разработке и дизайне сайтов.
                        В своих проектах мы используем технеологию дополненной реальности.
                        Это новый способ интерактивных развлечений, взаимодействия и общения с вашей аудиторией.
                        Попробуйте сами и убедитесь в этом!
                    </p>
                </div>
            </div>
        </div>
    </section>
    <article class="container third__container">
        <div class="row">
            <div class="col">
                <section class="ar_block">
                    <h2>Дополненная реалность уже в вашем телефоне</h2>
                    <section class="ar_block_1 ar">
                        <h3>Обьекты</h3>
                        <p>
                            Размещайте объекты, крутите, рассматривайт.
                            Позвольте своим клиентам почувствовать всю мощь дополнительной реальности
                        </p>
                        <button type="button" class="btn ar__button">Попробуйте Ar</button>
                    </section>
                    <section class="ar_block_2 ar">
                        <h3>Обьекты</h3>
                        <p>
                            Размещайте объекты, крутите, рассматривайт.
                            Позвольте своим клиентам почувствовать всю мощь дополнительной реальности
                        </p>
                        <button type="button" class="btn ar__button">Попробуйте Ar</button>
                    </section>
                </section>
            </div>
        </div>
    </article>
    <div class="container form__container">
        <div class="row">
            <div class="col-6">
                <div class="form_text">
                    <h2>Свяжитесь с нами</h2>
                    <p>
                        Мы дадим вам обратную связь в течении дня
                    </p>
                </div>
            </div>
            <div class="col-6 ">
                <div class="form">
                <form action="#" class="form_input">
                    <input type="text" class="form-control" placeholder="Ваше имя" require>
                    <input type="email" class="form-control" placeholder="Ваш email" require>
                    <button class="btn form__btn" type="submit">Отправить</button>
                </form>
            </div>
            </div>
        </div>
    </div>
</main>

<style lang="scss" >
    @import 'style/theme.scss';

    .container{
        position: relative;
        // width: 100%;
        color: $colorWhite;
        font-family: $opensans;
    }
    .first__container,
    .second__container{
        color: $colorWhite;
        font-family: $opensans;
        padding: 0px;
        margin: 0px;
        display: flex;
        margin-left:124px;
    }

    .first__container{
        display: flex;
        justify-content: center;
       align-items: center;
        margin-bottom: 240px;
        flex-direction: row;

    }

    .main_text{
        position: relative;
        margin-top: 300px;
    }

    .main_text h1{
font-family: $neohe;
font-size: 153px;
text-transform: uppercase;
// width: 1105px;
margin-bottom: -20px;

    }
    .main_text h3{
font-weight: 700;
font-size: 37px;
margin-bottom: 20px;
    }

.main_text p {
    font-size: 30px;
    margin-bottom: 70px;
    // width: 719px;
    // height: 105px;
}

.first__button{
    font-size: 31px;
    font-weight: 700;
    background-color: $dark-orange;
    color: $colorWhite;
    border-radius: 20px;
    // width: 391px;
    // height: 64px;
    display: flex;
    justify-content: center;
    box-shadow: 0px 0px 10px $dark-orange;
    text-transform: uppercase;


}

.video_block{
    position: absolute;
margin-top: 190px;
    border: 5px solid $colorWhite;
    // width: 700px;
    // height: 510px;
    margin-left: 950px;
    transform:skewX(-12DEG) skewY(-4DEG);
    filter: blur(1px);
}

.second__container{

margin-bottom: 400px;
}


.about_text h2{

font-weight: 700;
font-size: 115px;
// width: 705px;
// height: 199px;
line-height: 92.8%;
text-transform: uppercase;
margin-bottom:50px;
}

    .about_text p{
// width: 1200px;
// height: 190px;
font-size: 33px;
line-height: 115.3%;
    }





.ar_block{
 padding: 0px;
 margin: 0px;
display: flex;
flex-direction: column;
align-items: center;

}

.third__container{
    margin-bottom: 250px;
}

    .ar_block h2{

    position: absolute;
text-align: center;
font-weight: 700;
font-size: 96px;
text-transform: uppercase;
    }



    .ar{
        // width: 99vw;
        // height: 660px;
        background-image: url('/img/ar_block_1_img.jpg');
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center;
        margin-top: 500px;
        margin-bottom: 200px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

    }

    .ar h3{
        text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.7);
        text-transform: uppercase;
font-weight: 700;
font-size: 86px;
color: $colorWhite;

    }

    .ar p{
        // width: 1365px;
        display: flex;
        // height:150px;
        align-content: center;
font-weight: 700;
font-size: 36px;
margin-bottom: 100px;

    }

    .ar__button{
        color: $colorWhite;
        display: flex;
        justify-content: center;
        font-weight: 700;
        font-size: 48px;
        // width: 529px;
        // height: 100px;
        border: 5px solid $colorWhite;
        border-radius: 20px;


    }

    .ar_block_1{
        padding: 0px;
        margin-bottom: -440px;

    }
    .ar_block_2{
        // width: 99vw;
        // height: 660px;
        background-image: url('/img/ar_block_2_img.jpg');
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        margin-bottom: 60px;
    }


    .form__container{

        margin-left: 50px;

    }



    .form_text{
    margin-bottom: 600px;



    }


    .form_input{
        margin-top: -50px;
        border:10px solid $dark-orange;
        // width: 850px;
        // height: 400px;
    margin-left: 200px;
       display: flex;
       align-items: center;
       justify-content: center;
       flex-direction: column;

//        background: rgb(195,34,143);
// background: linear-gradient(0deg, rgba(195,34,143,1) 11%, rgba(241,253,45,1) 100%);

    }




    .form_text h2{


font-weight: 700;
font-size: 115px;
text-transform: uppercase;
line-height: 92.8%;

    }

    .form_text p{
        margin-top: 20px;
        font-size: 33px;
line-height: 115.3%;
// width: 785px;

    }

    .form-control{
        // width: 716px;
        // height: 75px;
        margin-bottom: 35px;
        font-size: 33px;
        line-height: 115.3%;
       padding-left:35px;
    }


input::-webkit-input-placeholder {
   color: $colorDark ;   ;
}
input:-moz-placeholder {
    color: $colorDark;
}
input::-moz-placeholder {
    color: $colorDark;
}
input:-ms-input-placeholder {
    color: $colorDark;
}


.form__btn{
    background-color: $dark-orange;
    color: $colorWhite;
    // width: 300px;
    // height: 60px;
    font-size: 36px;
    font-weight: 700;
    text-transform: uppercase;
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>
