<template>
  <p class="Title">Ты сегодня покормил кота? </p>
  <div class="Cards">
    <div class="Container">
      <div class="Card">
        <div class="CardItem">
          <label class="CheckboxOther">
            <input type="checkbox" id="cat1" @click="ChangeDescription()">
            <div class="CardBg"></div>
            <div class="CardStats">
              <div class="CardContainer">
                <div class="CardInfo">
                  <p class="CardInfoDescription CardInfoDescription--Default" id="cat1Default">Сказочное заморское явство</p>
                  <p class="CardInfoDescription" id="cat1Select">Котэ не одобряет?</p>
                  <h2 class="CardInfoTitle">Нямушка</h2>
                  <p class="CardInfoTeste">с фуа-гра</p>
                  <p class="CardInfoGift"><b>10</b> порций<br>
                    мышь в подарок
                  </p>
                </div>
              </div>
              <img class="CardCat" src="../assets/Cat.png">
              <div class="CardWigth">
                <p class="CardWigthCountZero">0,5</p>
                <p class="CardWigthMassa">кг</p>
              </div>
            </div>
            <p class="CardDescription CardDescription--sentense" id="CatDefault1">Чего сидишь? Порадуй котэ,
              <a class="CardDescription--buy">купи.</a>
            </p>
            <p class="CardDescription CardDescription--have" id="CatHave1">Печень утки разварная с артишоками.</p>
            <p class="CardDescription CardDescription--lose" id="CatLose1">Печалька, с фуа-гра закончился.</p>
          </label>
        </div>
      </div>

      <div class="Card">
        <div class="CardItem">
          <label class="CheckboxOther">
            <input type="Checkbox" id="cat2" @click="ChangeDescription()" checked>
            <div class="CardBg"></div>
            <div class="CardStats">
              <div class="CardContainer">
                <div class="CardInfo">
                  <p class="CardInfoDescription CardInfoDescription--Default">Сказочное заморское явство</p>
                  <p class="CardInfoDescription CardInfoDescription--Selected">Котэ не одобряет?</p>
                  <h2 class="CardInfoTitle">Нямушка</h2>
                  <p class="CardInfoTeste">с рыбой</p>
                  <p class="CardInfoGift"><b>40</b> порций<br>
                    <b>2</b> мыши в подарок
                  </p>
                </div>
              </div>
              <img class="CardCat" src="../assets/Cat.png">
              <div class="CardWigth">
                <p class="CardWigthCount">2</p>
                <p class="CardWigthMassa">кг</p>
              </div>
            </div>
            <p class="CardDescription CardDescription--sentense" id="CatDefault2">Чего сидишь? Порадуй котэ, <a
                class="CardDescription--buy">купи.</a></p>
            <p class="CardDescription CardDescription--have" id="CatHave2">Головы щучьи с чесноком да свежайшая
              сёмгушка.</p>
            <p class="CardDescription CardDescription--lose" id="CatLose2">Печалька, с рыбой закончился.</p>
          </label>
        </div>
      </div>

      <div class="Card">
        <div class="CardItem">
          <label class="CheckboxOther">
            <input type="Checkbox" id="cat3" @click="ChangeDescription()" disabled="disabled">
            <div class="CardBg"></div>
            <div class="CardStats">
              <div class="CardContainer">
                <div class="CardInfo">
                  <p class="CardInfoDescription CardInfoDescription--Default">Сказочное заморское явство</p>
                  <p class="CardInfoDescription CardInfoDescription--Selected">Котэ не одобряет?</p>
                  <h2 class="CardInfoTitle">Нямушка</h2>
                  <p class="CardInfoTeste">с курой</p>
                  <p class="CardInfoGift"><b>100</b> порций<br>
                    <b>5</b> мышией в подарок<br>
                    заказчик доволен
                  </p>
                </div>
              </div>
              <img class="CardCat" src="../assets/Cat.png">
              <div class="CardWigth">
                <p class="CardWigthCount">5</p>
                <p class="CardWigthMassa">кг</p>
              </div>
            </div>
            <p class="CardDescription CardDescription--sentense" id="CatDefault3">Чего сидишь? Порадуй котэ,
              <a class="CardDescription--buy">купи.</a>
            </p>
            <p class="CardDescription CardDescription--have" id="CatHave3">Филе из цыплят с трюфелями в бульоне.</p>
            <p class="CardDescription CardDescription--lose" id="CatLose3">Печалька, с курой закончился.</p>
          </label>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Home',
  methods: {
    ChangeDescription: function () {
      //console.log(cat1.disabled,cat1.checked)
      if (cat1.disabled) {
        document.getElementById('CatDefault1').style.display = 'none'
        document.getElementById('CatHave1').style.display = 'none'
        document.getElementById('CatLose1').style.display = 'block' 
      }
      else {
        document.getElementById('CatLose1').style.display = 'none'
        if (cat1.checked) {
          document.getElementById('CatDefault1').style.display = 'none'
          document.getElementById('CatHave1').style.display = 'block'
          document.getElementById('cat1Default').classList.add("HelpBlock")
          this.AddClass();
        }
        else {
          document.getElementById('cat1Select').classList.remove("CardInfoDescription--Selected")
          document.getElementById('CatDefault1').style.display = 'block'
          document.getElementById('CatHave1').style.display = 'none'
        }
      }
      //console.log(cat2.disabled,cat2.checked)
      if (cat2.disabled) {
        document.getElementById('CatDefault2').style.display = 'none'
        document.getElementById('CatHave2').style.display = 'none'
        document.getElementById('CatLose2').style.display = 'block'
      }
      else {
        document.getElementById('CatLose2').style.display = 'none'
        if (cat2.checked) {
          document.getElementById('CatDefault2').style.display = 'none'
          document.getElementById('CatHave2').style.display = 'block'
        }
        else {
          document.getElementById('CatDefault2').style.display = 'block'
          document.getElementById('CatHave2').style.display = 'none'
        }
      }
      //console.log(cat3.disabled,cat3.checked)
      if (cat3.disabled) {
        document.getElementById('CatDefault3').style.display = 'none'
        document.getElementById('CatHave3').style.display = 'none'
        document.getElementById('CatLose3').style.display = 'block'
      }
      else {
        document.getElementById('CatLose3').style.display = 'none'
        if (cat3.checked) {
          document.getElementById('CatDefault3').style.display = 'none'
          document.getElementById('CatHave3').style.display = 'block'
        }
        else {
          document.getElementById('CatDefault3').style.display = 'block'
          document.getElementById('CatHave3').style.display = 'none'
        }
      }
    },
    AddClass: function(){
      document.getElementById('cat1Default').classList.remove("HelpBlock")
      document.getElementById('cat1Select').classList.add("CardInfoDescription--Selected")
    }
  },
  mounted: function () {
    this.ChangeDescription();
  }
}
</script>
<style>
@import './Style.css'
</style>
