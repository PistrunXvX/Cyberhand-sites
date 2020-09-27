<script>
    import Typewriter from 'svelte-typewriter';
    import { draw } from 'svelte/transition';
    import { quintOut } from 'svelte/easing';
    let condition = false;
    setTimeout(() => condition = true);

    let coordX;
    let coordY

    function coordsCleint(e){
        coordX = Math.round(e.offsetX);
        coordY = Math.round(e.offsetY);
        console.log(coordX);
    };

    $: style = `
        background-position-x: calc(80% + (${coordY}%  / 100)), calc(50% + (${coordY}%  / 100));
        background-position-y: calc(50% + (${coordX}% / 100)), calc(20% + (${coordY}%  / 100));
  `;

    let isScrolling = false;

    window.addEventListener("scroll", throttleScroll, false);

    function throttleScroll(e) {
        if (isScrolling == false ) {
            window.requestAnimationFrame(function() {
            scrolling(e);
            isScrolling = false;
            });
        }
        isScrolling = true;
    };

    document.addEventListener("DOMContentLoaded", scrolling, false);

    let secondBox = document.querySelector("#animation__container");

    function scrolling(e){
        if (isPartiallyVisible(secondBox)) {
        secondBox.classList.add("active");
      }
    };

    function isPartiallyVisible(el) {
      let elementBoundary = el.getBoundingClientRect();

      let top = elementBoundary.top;
      let bottom = elementBoundary.bottom;
      let height = elementBoundary.height;

      return ((top + height >= 0) && (height + window.innerHeight >= bottom));
    };

    function isFullyVisible(el) {
      let elementBoundary = el.getBoundingClientRect();

      let top = elementBoundary.top;
      let bottom = elementBoundary.bottom;

      return ((top >= 0) && (bottom <= window.innerHeight));
    };

function dealWithScrolling(e) {
    // do epic stuff
}
</script>

<main>
    <section class="container first__container">
        <div class="row">
            <div class="col">
                <div class="main_text">
                   
                    <h1>Cyber Hand</h1>
                    <Typewriter cascade interval={50}>
                    <h3>Ваш сайт - наша работа</h3>
                    <p>
                        Создаем интерфейсы аналитических систем, мобильные приложения и цифровые сервисы для государства и крупного бизнеса
                    </p>
                    </Typewriter>
                    <a type="button" class="btn first__button">Свяжитесь с нами</a>
                </div>
            </div>
            <!-- <div class="col-lg-4 video_block">
                <video src="#"></video>
            </div> -->
        </div>
    </section>
    <section class="container second__container" id="animation__container" on:mousemove={coordsCleint} {style}>
        <div class="row">
            <div class="col-lg-12">
                <div class="about_text">
                    <h2>О нашей <br> студии</h2>
                    <p>
                        Мы - небольшая веб-студия и группа единомышленников. <br> Специализируемся на разработке и дизайне сайтов.
                        <br> В своих проектах мы используем технеологию дополненной реальности.
                        <br> Это новый способ интерактивных развлечений, взаимодействия и общения с вашей аудиторией.
                         Попробуйте сами и убедитесь в этом!
                    </p>
                </div>
            </div>
        </div>
    </section>
    <article class=" third__container container-fluid">
        <div class="draw__line__3">
            <svg>
                {#if condition}
                <path 
                    in:draw="{{delay: 1000, duration: 2000, easing: quintOut}}"
                    d="M 0 0 L 250 100"
                    style="stroke:#F2AE00; stroke-width: 5;" 
                />
            {/if}
            </svg>
        </div>
        <div class="draw__line__4">
            <svg>
                {#if condition}
                <path 
                    in:draw="{{delay: 1000, duration: 2000, easing: quintOut}}"
                    d="M 0 0 L 250 100"
                    style="stroke:#F2AE00; stroke-width: 5;" 
                />
            {/if}
            </svg>
        </div>
        <div class="row">
            <div class="col-lg-12">
                <section class="ar_block">
                    <h2>Дополненная реалность уже в вашем телефоне</h2>
                    <section class="ar_block_1 ar">
                        <h3>3D обьекты</h3>
                        <p>
                            Размещайте объекты, крутите, рассматривайт.
                            Позвольте своим клиентам почувствовать всю мощь дополнительной реальности
                        </p>
                        <div class="button_ar">
                            <a href="#" class="btn ar__button" >Попробуйте Ar</a>
                        </div>
                    </section>
                    <section class="ar_block_2 ar">
                        <h3>Взаимодействуйте</h3>
                        <p>
                            С помощью маркеров вы получите возможность по новому взглянуть на способ взаимодействия с вашей информацией
                        </p>
                        <div class="button_ar">
                            <a href="#" class="btn ar__button">Попробуйте Ar</a>
                        </div>
                    </section>
                </section>
            </div>
        </div>
    </article>
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
</main>

<style lang="scss" >
    @import 'style/theme.scss';
    @import 'style/resize.scss';

    .main_text{

        h1{
            font-family: $neohe;
            font-size: $fontBigH1;
            color: $colorWhite;

            text-transform: uppercase;

        }

        h3{
            font-family: $opensans;
            font-size: 37px;
            color: $colorWhite;
        }
        p{
            font-family: $opensans;
            font-size: $fontBigP;
            color: $colorWhite;

            line-height: 115.3%;
        }
    }

    .first__container{
        margin-top: 15%;

        animation: 1s ease-in 0s 1 alternate opacity;

        .first__button{
            font-family: $opensans;
            font-size: $fontBigP;
            color: $colorWhite;

            background: $colorYellow;
            border-radius: 20px;
            transition: background 0.5s, box-shadow 0.5s;

            padding: 1% 5%;
            margin-top: 3%;

            box-shadow: 0px 0px 10px #F2AE00;
        }

        .first__button:hover{
            background: #1D002B;
            box-shadow: 0px 0px 10px $colorWhite;
        }
    }

    .second__container{
        margin-top: 15%;

        background-image: url("/img/about_1.png"),
                          url("/img/about_2.png");
        background-size: 300px, 300px;
        background-repeat: no-repeat, no-repeat;
        background-position: 80%, 50%, 50%, 20%;
    }

    .about_text{

        h2{
            font-family: $opensans;
            font-size: $fontBigH2;
            color: $colorWhite;
            font-weight: bold;

            text-transform: uppercase;
        }

        p{
            font-family: $opensans;
            font-size: $fontBigP;
            color: $colorWhite;

            line-height: 115.3%;
        }
    }

    .active{
        animation: 1s ease-in 0s 1 alternate opacity;
    }

    .third__container{
        margin-top: 15%;
        position: relative;
    }

    .ar_block{

        h3{
                font-family: $opensans;
                font-size: $fontBigH3;
                color: $colorWhite;
                font-weight: bold;

                text-transform: uppercase;
                text-align: center;

                padding-top: 10%;
                text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.7);
            }

            p{
                font-family: $opensans;
                font-size: $fontBigP;
                color: $colorWhite;
                font-weight: bold;

                text-align: center;
                line-height: 103.3%;

                padding-bottom: 5%;
            }

        h2{
            font-family: $opensans;
            // font-size: 80px;
            font-size: $fontBigH3;
            color: $colorWhite;
            font-weight: bold;

            text-transform: uppercase;
            text-align: center;
        }

        .ar_block_1{
            background-image: url("/img/ar_block_1_img.jpg");
            background-size: cover;
            background-repeat: no-repeat;

            margin-bottom: 5%;
        }

        .ar_block_2{
            background-image: url("/img/ar_block_2_img.jpg");
            background-size: cover;
            background-repeat: no-repeat;
        }
    }

    .button_ar{
        text-align: center;
        padding-bottom: 5%;
    }

    .ar__button{
            font-family: $opensans;
            // font-size: 36px;
            font-size: 36px;
            color: $colorWhite;
            font-weight: bold;

            background-color: none;
            border-color: white;
            border-width: 3px;
            border-radius: 20px;
            color: white;

            padding-right: 5%;
            padding-left: 5%;
        }

    .ar__button:hover{
        color: black;
        background-color: $colorWhite;
        border-color: black;
    }

    .four__container{
        padding-bottom: 25%;
        margin-top: 20%;
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

.draw__line__3{
		position: absolute;
		top: 0;
    }
    
    .draw__line__4{
		position: absolute;
        top: 5%;
	}





    @keyframes opacity{
        from{
            opacity: 0;
        }
        to{
            opacity: 1;
        }
    }


//     .container{
//         position: relative;
//         width: 100vw;
//         color: $colorWhite;
//         font-family: $opensans;
//     }
//     .first__container,
//     .second__container{
//         color: $colorWhite;
//         font-family: $opensans;
//         padding: 0px;
//         margin: 0px;
//         display: flex;
//         margin-left:124px;
//     }

//     .first__container{
//         display: flex;
//         justify-content: center;
//        align-items: center;
//         margin-bottom: 240px;
//         flex-direction: row;

//     }

//     .main_text{
//         position: relative;
//         margin-top: 300px;
//     }

//     .main_text h1{
// font-family: $neohe;
// font-size: 153px;
// text-transform: uppercase;
// width: 1105px;
// margin-bottom: -20px;

//     }
//     .main_text h3{
// font-weight: 700;
// font-size: 37px;
// margin-bottom: 20px;
//     }

// .main_text p {
//     font-size: 30px;
//     margin-bottom: 70px;
//     width: 719px;
//     height: 105px;
// }

// .first__button{
//     font-size: 31px;
//     font-weight: 700;
//     background-color: $dark-orange;
//     color: $colorWhite;
//     border-radius: 20px;
//     width: 391px;
//     height: 64px;
//     display: flex;
//         justify-content: center;
//     box-shadow: 0px 0px 10px $dark-orange;
//     text-transform: uppercase;


// }

// .video_block{
//     position: absolute;
// margin-top: 190px;
//     border: 5px solid $colorWhite;
//     width: 700px;
//     height: 510px;
//     margin-left: 950px;
//     transform:skewX(-12DEG) skewY(-4DEG);
//     filter: blur(1px);
// }

// .second__container{

// margin-bottom: 400px;
// }


// .about_text h2{

// font-weight: 700;
// font-size: 115px;
// width: 705px;
// height: 199px;
// line-height: 92.8%;
// text-transform: uppercase;
// margin-bottom:50px;
// }

//     .about_text p{
// width: 1200px;
// height: 190px;
// font-size: 33px;
// line-height: 115.3%;
//     }





// .ar_block{
//     padding: 0px;
//     margin: 0px;
// display: flex;
// flex-direction: column;
// align-items: center;

// }
// .ar_block_1{


// }

//     .ar_block h2{

//         position: absolute;
//         text-align: center;
// font-weight: 700;
// font-size: 96px;
// text-transform: uppercase;
//     }



//     .ar{
//         width: 99vw;
//         height: 660px;
//         background-image: url('/img/ar_block_1_img.jpg');
//         background-size: cover;
//         background-repeat: no-repeat;
//         background-position: center;
//         margin-top: 500px;
//         margin-bottom: 200px;
//         display: flex;
//         flex-direction: column;
//         justify-content: center;
//         align-items: center;

//     }

//     .ar h3{
//         text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.7);
//         text-transform: uppercase;
// font-weight: 700;
// font-size: 86px;
// color: $colorWhite;
//     }

//     .ar p{
//         width: 1365px;
//         display: flex;
//         height:150px;
//         align-content: center;
// font-weight: 700;
// font-size: 36px;
// margin-bottom: 100px;
//     }

//     .ar__button{
//         color: $colorWhite;
//         display: flex;
//         justify-content: center;
//         font-weight: 700;
//         font-size: 48px;
//         width: 529px;
//         height: 100px;
//         border: 5px solid $colorWhite;
//         border-radius: 20px;


//     }

//     .ar_block_1{
//         padding: 0px;
//         margin-bottom: -440px;

//     }
//     .ar_block_2{
//         width: 99vw;
//         height: 660px;
//         background-image: url('/img/ar_block_2_img.jpg');
//         background-size: cover;
//         background-repeat: no-repeat;
//         background-position: center;
//         display: flex;
//         flex-direction: column;
//         justify-content: center;
//         align-items: center;
//         margin-bottom: 60px;
//     }


    // .form__container{

    //     margin-left: 50px;

    // }



    // .form_text{
    // margin-bottom: 600px;



    // }


    // .form_input{
    //     margin-top: -50px;
    //     border:10px solid $dark-orange;
    //     width: 850px;
    //     height: 400px;
    // margin-left: 200px;
    //    display: flex;
    //    align-items: center;
    //    justify-content: center;
    //    flex-direction: column;

//        background: rgb(195,34,143);
// background: linear-gradient(0deg, rgba(195,34,143,1) 11%, rgba(241,253,45,1) 100%);

    // }




//     .form_text h2{


// font-weight: 700;
// font-size: 115px;
// text-transform: uppercase;
// line-height: 92.8%;

//     }

//     .form_text p{
//         margin-top: 20px;
//         font-size: 33px;
// line-height: 115.3%;
// width: 785px;

//     }

//     .form-control{
//         width: 716px;
//         height: 75px;
//         margin-bottom: 35px;
//         font-size: 33px;
//         line-height: 115.3%;
//        padding-left:35px;
//     }


// input::-webkit-input-placeholder {
//    color: $colorDark ;   ;
// }
// input:-moz-placeholder {
//     color: $colorDark;
// }
// input::-moz-placeholder {
//     color: $colorDark;
// }
// input:-ms-input-placeholder {
//     color: $colorDark;
// }


// .form__btn{
//     background-color: $dark-orange;
//     color: $colorWhite;
//     width: 300px;
//     height: 60px;
//     font-size: 36px;
//     font-weight: 700;
//     text-transform: uppercase;
//     display: flex;
//     justify-content: center;
//     align-items: center;
// }
</style>
