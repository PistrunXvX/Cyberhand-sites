<script>

</script>

<div class="container-fluid">
    <div class="container">
        <div class="row">
            <div class="col">
                <h1>Услуги</h1>
            </div>
        </div>
        <div class="accordion row" id="accordion">
          <div class="col-12">
            <div class="">
              <div class="card-header" id="headingOne">
                <h2 class="mb-0">
                  <button class="btn btn-block text-left" type="button" data-toggle="collapse" data-target="#collapseBlock_1" aria-expanded="true" aria-controls="collapseBlock_1">
                    Разработка и поддержка веб сайта
                  </button>
                </h2>
              </div>
          
              <div id="collapseBlock_1" class="collapse" aria-labelledby="headingOne" data-parent="#accordion">
                <div class="card-body">
                  <ul>
                    <li>Разрабатываем продукты разной сложности</li>
                    <li>Поддерживаем весь жизненный цикл разработки</li>
                    <li>Составим грамотное техническое задание</li>                      
                  </ul>
                </div>
              </div>
            </div>
          </div>
          <div class="col-12">
            <div class="">
              <div class="card-header" id="headingTwo">
                <h2 class="mb-0">
                  <button class="btn btn-block text-left" type="button" data-toggle="collapse" data-target="#collapseBlock_2" aria-expanded="true" aria-controls="collapseBlock_2">
                    Разработка индивидуального дизайна
                  </button>
                </h2>
              </div>
          
              <div id="collapseBlock_2" class="collapse" aria-labelledby="headingTwo" data-parent="#accordion">
                <div class="card-body">
                  <ul>
                    <li>Продумываем интерфейсы и взаимодействие клиента</li>
                    <li>Создаем фотобазы</li>
                    <li>Используем последние тренды</li>                      
                  </ul>
                </div>
              </div>
            </div>
          </div>
          <div class="col-12">
            <div class="">
              <div class="card-header" id="headingThree">
                <h2 class="mb-0">
                  <button class="btn btn-block text-left" type="button" data-toggle="collapse" data-target="#collapseBlock_3" aria-expanded="true" aria-controls="collapseBlock_3">
                    SEO/SMM продвижение
                  </button>
                </h2>
              </div>
          
              <div id="collapseBlock_3" class="collapse" aria-labelledby="headingThree" data-parent="#accordion">
                <div class="card-body">
                  <ul>
                    <li>Настройка контекстной и таргетированной рекламы</li>
                    <li>Продвижение в социальных сетях</li>
                    <li>Аналитика и привлечение аудитории</li>                      
                  </ul>
                </div>
              </div>
            </div>
          </div>
        </div>
    </div>
</div>
<style lang="scss">
    @import "../style/theme.scss";
    @import "../style/resize.scss";

    .container-fluid{
      background-color: $darkColor;
      padding-top: 10%;

      h1{
        font-size: $fontBigH1;
        font-family: $opensans;
        font-weight: bold;
        color: $colorWhite;
      }

      button{
        font-size: $fontBigP;
        font-family: $opensans;
        color: $colorWhite;
      }

      .col-12{
        margin-top: 5%;
      }

      .col-12:last-child{
        padding-bottom: 5%;
      }

      li{
        font-size: $fontBigP;
        font-family: $opensans;
        color: $colorWhite;

        list-style: none;
      }

      li:before{
        content:"-";
        padding-right: 10px;
      }
    }

</style>
