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
    <article class="container">
        <div class="row">
            <div class="col">
                <section class="ar_block">
                    <h2>Дополненная реалность уже в вашем телефоне</h2>
                    <section class="ar_block_1">
                        <h3>Обьекты</h3>
                        <p>
                            Размещайте объекты, крутите, рассматривайт. 
                            Позвольте своим клиентам почувствовать всю мощь дополнительной реальности
                        </p>
                    </section>
                    <section class="ar_block_2">
                        <h3>Обьекты</h3>
                        <p>
                            Размещайте объекты, крутите, рассматривайт. 
                            Позвольте своим клиентам почувствовать всю мощь дополнительной реальности
                        </p>
                    </section>
                </section>
            </div>
        </div>
    </article>
    <div class="container">
        <div class="row">
            <div class="col-6">
                <div class="form_text">
                    <h2>Свяжитесь с нами</h2>
                    <p>
                        Мы дадим вам обратную связь в течении дня
                    </p>
                </div>
            </div>
            <div class="col-6">
                <form action="#">
                    <input type="text" class="form-control" placeholder="Ваше имя" require>
                    <input type="email" class="form-control" placeholder="Ваш email" require>
                    <button class="btn" type="submit">Отправить</button>
                </form>
            </div>
        </div>
    </div>
</main>

<style lang="scss" >
    @import 'style/theme.scss';
    
    .container{
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
width: 1105px;
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
    width: 719px;
    height: 105px;
}

.first__button{
    font-size: 31px;
    font-weight: 700;
    background-color: $dark-orange;
    color: $colorWhite;
    border-radius: 20px;
    width: 391px;
    height: 64px;
    text-align: center;
    box-shadow: 0px 0px 10px $dark-orange;
    text-transform: uppercase;
    
    
}

.video_block{
    position: absolute;
margin-top: 190px;
    border: 5px solid $colorWhite;
    width: 700px;
    height: 510px;
    margin-left: 950px;
    transform:skewX(-12DEG) skewY(-4DEG);
    filter: blur(1px);
}

.second__container{

margin-bottom: 240px;
}


.about_text h2{

font-weight: 700;
font-size: 115px;
width: 705px;
height: 199px;
line-height: 92.8%;
text-transform: uppercase;
margin-bottom:50px;
}

    .about_text p{
width: 1200px; 
height: 190px;
font-size: 33px;
line-height: 115.3%;

    }
</style>
