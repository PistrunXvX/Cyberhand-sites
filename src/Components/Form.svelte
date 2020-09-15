
<div class="container-fluid">
<div class="container four__container">
    <div class="row">
        <div class="col-lg-6 col-sm-12 col-xs-12 ">
            <div class="form_text">
                <h2>Свяжитесь<br> с нами</h2>
                <p>
                    Мы дадим вам обратную связь в течении дня
                </p>
            </div>
        </div>
        <div class="col-lg-6 col-sm-12m col-xs-12">
            <div class="form">
            <form action="#" class="form_input">
                <input type="text" class="form-control" placeholder="Ваше имя" require>
                <input type="email" class="form-control" placeholder="Ваш email" require>
                <div class="text-center">
                <button class="btn form__btn" type="submit">Отправить</button>
                </div>
            </form>
        </div>
        </div>
    </div>
</div>
</div>
<style lang="scss">
 @import 'style/theme.scss';
@import 'style/resize.scss';


.container-fluid{
    background-color: $darkColor;
}
.four__container{
        padding-bottom: 25%;
        padding-top: 20%;
        
    }

    .form_text{

    margin-top: 10%;

        h2{
            font-family: $opensans;
            // font-size: 95px;
            font-size: $fontBigH3;
            color: $colorWhite;
            font-weight: 700;
            text-transform: uppercase;
            line-height: 92.8%;
        }

        p{
            font-family: $opensans;
            font-size: 18px;
            color: $colorWhite;
        }
    }



.form{
    padding: 6%;
    border: 8px solid transparent;
    border-image: linear-gradient(to right, #c3228f 0%, #eeec35 100%);
    border-image-slice: 1;

}

.form-control{
    font-size: 27px;
    padding: 3% 6%;
    margin-bottom: 5%;
    line-height: 115.3%;
    font-family: $opensans;
    border:none;
    border:bottom 1px solid #757575;
    transition: background-color 0.2s ease-in;
}

.form-control:focus{
    transition: background-color 0.2s ease-in;
   background-color: #fff3c9;
}
.form__btn{
    background-color: $dark-orange;
    color: $colorWhite;
    text-transform: uppercase;
    // font-size: 30px;
    font-size: $fontBigP;
    font-weight: 700;
    padding: 1% 10%;
    margin-top: 3%;
    transition: all 0.4s ease-out;

}

.form__btn:hover{
    transition: all 0.4s ease-out;
    background: none;
    border-radius:5px;
box-shadow: 0px 5px  65px #c3238f;
}

input::-webkit-input-placeholder {
   color: $darkColor;   ;
}
input:-moz-placeholder {
    color:$darkColor;
}
input::-moz-placeholder {
    color:$darkColor;
}
input:-ms-input-placeholder {
    color:$darkColor;
}


</style>