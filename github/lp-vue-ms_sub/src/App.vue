<template>
  <div id="app">
    <CommonHeader></CommonHeader>
    <main>
      <div id="eyecatch">
        <div class="p">
          <p>機械ではできない仕事を</p>
        </div>
        <div class="news1">
          <p>2019/01/01</p>
          <p>ニュースタイトルがここに入ります。3月の決算報告書</p>
        </div>
        <div class="news2">
          <p>news</p>
        </div>
      </div>
      <div id="about" class="wrap">
        <div class="mission">
          <div class="mission-img">
              <img src="../src/assets/mission-img.jpg" />
            </div>
          <p class="mission-title">お客様のために進化する成長企業であり続ける</p>
          <p class="mission-text">顧客主導型サービスを提供する企業として、お客様の会社経営に必要なサービスと情報を提供し続ける企業支援会社を目指します。企業が現在直面している「勝ち残るため」の戦略を提供できる会社として、ホームページをはじめ、各種マーケティングをご提供いたします。</p>
          <a class="link" href="#">ミッション詳細</a>
        </div>
      </div>
      <div id="service">
        <h2 class="section-title">service</h2>
        <div id="service-desktop">
            <div class="sd1">
                
                <h2 class="sd1-title">web制作事業</h2>
                <p class="sd1-sub">
                    コーチングのミッション
                </p>
                <p class="sd1-des">ユーザーが求める物を分析し、ユーザビリティを備えた最適なサイトを提供。建設業から美容、ブライダル、飲食店まで多種多様な業種の制作実績があります。</p>
                <a class="sd1-button">サービス詳細</a>
            </div>
                <div class="sd1-img">
                    <img src="./assets/service2.jpg"/>
                </div>
            <div class="sd2">
                <h2 class="sd2-title">web制作事業</h2>
                <p class="sd2-sub">
                    コーチングのミッション
                </p>
                <p class="sd2-des">ユーザーが求める物を分析し、ユーザビリティを備えた最適なサイトを提供。建設業から美容、ブライダル、飲食店まで多種多様な業種の制作実績があります。</p>
            </div>
            <div class="sd2-img">
                    <img src="./assets/service1.jpg" />
                </div>
        </div>
        <div class="service-wrap">
          <div class="servicecard1">
            <div class="service-card" v-for="(data,index) in service" :key="index">
              <img class="service-img" :src="data.img" alt />
              <h2>{{data.title}}</h2>
              <p class="sub">{{data.subtitle}}</p>
              <p class="des">{{data.description}}</p>
              <a class="s-button" href="#">{{data.button}}</a>
              
            </div>
          </div>
        </div>
      </div>
      <div id="company">
        <div class="f-contein">
          <div class="overview">
            <div class="photo2">
              <img src="../src/assets/company.jpeg" />
            </div>
            <div class="text">
              <h2>company</h2>
              <p>会社概要</p>
            </div>
          </div>
          <div class="recruit">
            <div class="photo3">
              <img src="../src/assets/recruit.jpg" />
            </div>
            <div class="text">
              <h2>recruit</h2>
              <p>採用情報</p>
            </div>
          </div>
        </div>
        <div class="FAQ">
          <h2>FAQ</h2>
          <p>良くある質問</p>
        </div>
      </div>
      <div id="contact">
        <h2 class="section-title">contact</h2>
        <div class="texts">
          <h3>お問い合わせ</h3>
          <p class="large-p">お気軽にお問い合わせください。</p>
          <p>
            資料請求・お問い合わせなどなんでも気軽にお問い合わせください。お仕事のご連絡もお問い合わせページに飛んでいただいて、入力フォームにご記入お願いいたします。
          </p>
          <a class="link-contact" href="#">お問い合わせへ</a>
        </div>
      </div>
    </main>
    <div id="footer-head">
      <span></span>
      <CommonHeader></CommonHeader>
    </div>
    <CommonFooter></CommonFooter>
  </div>
</template>

<script>
import CommonHeader from "./components/CommonHeader"
import CommonFooter from "./components/CommonFooter"
export default {
  data () {
    return {
      service: [
        {
          img: require("./assets/service2.jpg"),
          title: "web制作事業",
          subtitle: "コーチングのミッション",
          description:
            "ユーザーが求める物を分析し、ユーザビリティを備えた最適なサイトを提供。建設業から美容、ブライダル、飲食店まで多種多様な業種の制作実績があります。",
          button: "サービス詳細"
        },
        {
          img: require("./assets/service1.jpg"),
          title: "web制作事業",
          subtitle: "コーチングのミッション",
          description:
            "ユーザーが求める物を分析し、ユーザビリティを備えた最適なサイトを提供。建設業から美容、ブライダル、飲食店まで多種多様な業種の制作実績があります。",
            button: "サービス詳細"
        }
      ]
    };
  },
  components: {
    CommonHeader,
    CommonFooter
  }
};
</script>

<style>
/*リセットCSS */
html, body, div, span, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
abbr, address, cite, code,
del, dfn, em, img, ins, kbd, q, samp,
small, strong, sub, sup, var,
b, i,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, figcaption, figure,
footer, header, hgroup, menu, nav, section, summary,
time, mark, audio, video {
    margin:0;
    padding:0;
    border:0;
    outline:0;
    font-size:100%;
    vertical-align:baseline;
    background:transparent;
}

body {
    line-height:1;
}

article,aside,details,figcaption,figure,
footer,header,hgroup,menu,nav,section {
    display:block;
}

nav ul {
    list-style:none;
}

blockquote, q {
    quotes:none;
}

blockquote:before, blockquote:after,
q:before, q:after {
    content:'';
    content:none;
}

a {
    margin:0;
    padding:0;
    font-size:100%;
    vertical-align:baseline;
    background:transparent;
}

/* change colours to suit your needs */
ins {
    background-color:#ff9;
    color:#000;
    text-decoration:none;
}

/* change colours to suit your needs */
mark {
    background-color:#ff9;
    color:#000;
    font-style:italic;
    font-weight:bold;
}

del {
    text-decoration: line-through;
}

abbr[title], dfn[title] {
    border-bottom:1px dotted;
    cursor:help;
}

table {
    border-collapse:collapse;
    border-spacing:0;
}

/* change border colour to suit your needs */
hr {
    display:block;
    height:1px;
    border:0;  
    border-top:1px solid #cccccc;
    margin:1em 0;
    padding:0;
}

input, select {
    vertical-align:middle;
}

/* 共通のスタイル */

.section-title {
    font-size: 30px;
    font-weight: bold;
    margin: 30px 0;
    text-align: center;
}

img {
    display: block;
    width: 100%;
}

.wrap {
    width: 80%;
    margin: 0 auto 50px;
}

.flex {
    display: flex;
    align-items: center;
    flex-wrap: wrap;
}

.between {
    justify-content: space-between;
}

.around {
    justify-content: space-around;
}

/* 以下に各々のスタイル */

/* main */

/* eyecatch */
#eyecatch {
    height: 600px;
    background-image: url("../src/assets/eyecatch.jpg");
    background-size: cover;
    background-position: center;
    position: relative;
}

#eyecatch .p {
    position: absolute;
    top: 60%;
    left: 35%;
    transform: translate(-50%, -50%);
    font-size: 35px;
    font-style: italic;
    font-weight: bold;
    color: white;
    line-height: 1;
}

.news1 {
    width: 50%;
    height: 50px;
    background-color: white;
    position: relative;
    top: 550px;
    left: 50%;
    text-align: left;
    line-height: 25px;
}

.news2 {
    width: 100px;
    height: 50px;
    color: white;
    text-align: center;
    line-height: 50px;
    background-color: black;
    position: absolute;
    top: 550px;
    right: 0;
}


/* about */
#about {
    background-color: black;
    width: 100%;
    height: 450px;
}

.mission-title {
    color: white;
    font-size: large;
    font-weight: bold;
    margin: 10px;
    position: relative;
    top: -170px;
    left: 40px;
}

.mission p {
    color: white;
    position: relative;
    width: 65%;
    top: -160px;
    left: 50px;
}

.link {
    padding: 5px 30px;
    font-size: 14px;
    color: black;
    background-color: white;
    text-decoration: none;
    cursor: pointer;
    transition: 0.4s ease;
    position: relative;
    top: -140px;
    left: 50px;
}

.mission img {
    width: 45%;
    height: 350px;
    position: relative;
    top: 150px;
    left: 50%;
}

/* service */

#service {
    background-color: whitesmoke;
    padding: 5px 0;
    margin: 50px 0;
}

/* service-desktop */

.service-desktop {
    position: relative;
    margin: 0;
}

.sd1 {
    width: 50%;
    height: 250px;
    position: relative;
    left: 100px;
    top: 50px;
    color: #000;
    background-color: #ffffff;
}

.sd1-title {
    position: absolute;
    top: 50px;
    left: 100px;
    font-size: 18px;
    font-weight: bold;
}

.sd1-sub {
    position: absolute;
    top: 85px;
    left: 100px;
    width: 60%;
}

.sd1-des {
    position: absolute;
    top: 120px;
    left: 100px;
    width: 60%;
    line-height: 18px;
}

.sd1-button {
    padding: 5px 20px;
    font-size: 14px;
    color: #000;
    background-color: #ffffff;
    cursor: pointer;
    border: 1px #000 solid;
    transition: 0.4s;
    position: absolute;
    top: 200px;
    right: 150px;
}

.sd1-img {
    width: 50%;
    height: 600px;
    margin-left: auto;
    margin-top: -250px;
}

.sd2 {
    width: 50%;
    height: 250px;
    position: relative;
    left: 40%;
    top: 25px;
    color: #000;
    background-color: #ffffff;
}

.sd2-title {
    position: absolute;
    top: 50px;
    left: 100px;
    font-size: 18px;
    font-weight: bold;
}

.sd2-sub {
    position: absolute;
    top: 85px;
    left: 100px;
    width: 60%;
}

.sd2-des {
    position: absolute;
    top: 120px;
    left: 100px;
    width: 60%;
    line-height: 18px;
}

.sd2-button {
    padding: 5px 20px;
    font-size: 14px;
    color: #000;
    background-color: #ffffff;
    cursor: pointer;
    border: 1px #000 solid;
    transition: 0.4s;
    position: absolute;
    top: 200px;
    right: 150px;
}

.sd2-img {
    width: 50%;
    height: 400px;
    margin-right: auto;
    margin-top: -250px;
}

/* servicecard1 */

.service-wrap {
    display: none;
}

/* company */

#company {
    background-color: white;
    padding: 100px 0;
    width: 100%;
}

.f-contein {
    display: flex;
    justify-content: space-between;
}

.overview {
    position: relative;
    width: 47.5%;
    height: 100px;
    margin-right: auto;
}

.photo2 img {
    width: 100%;
    height: 200px;
}

.text h2 {
    color: white;
    font-size: 18px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}

.text p {
    color: white;
    position: absolute;
    font-size: 14px;
    top: 70%;
    left: 50%;
    transform: translate(-50%, -50%);
}


.recruit {
    position: relative;
    width: 47.5%;
    height: 100px;
}

.photo3 img {
    width: 100%;
    height: 200px;
}

.FAQ {
    background-color: black;
    margin: 200px 15% 0;
    height: 80px;
    width: 70%;
    display: flex;
    justify-content: center;
    position: relative;
}

.FAQ h2 {
    font-size: 24px;
    color: white;
    position: absolute;
    top: 50%;
    left: 8%;
    transform: translate(-50%, -50%);
}

.FAQ p {
    color: white;
    font-size: 14px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}

/* contact */

#contact {
    background-image: url("../src/assets/contact-bg.jpg");
    background-size: cover;
    background-position: center;
    color: white;
    height: 500px;
    width: 100%;
    padding: 100px 0;
}

.texts{
    margin: 130px;
}

#contact h3 {
    text-align: center;
    padding: 0 0 25px;
}

#contact .large-p {
    text-align: center;
    font-size: 32px;
    font-weight: normal;
    padding: 0 0 20px;
}

#contact p {
    text-align: center;
    font-size: 12px;
}

.link-contact {
    padding: 5px 20px;
    margin: 30px;
    font-size: 14px;
    color: white;
    text-decoration: none;
    cursor: pointer;
    border: 1px #ffffff solid;
    transition: 0.3s ease;
    position: absolute;
    left: 47.5%;
    transform: translate(-50%, -50%);
}




/* レスポンシブデザインのCSS */

@media screen and (max-width: 768px) {
   

    /* main */

    /* eyecatch */

    #eyecatch .p {
        width: 75%;
        text-align: center;
        position: absolute;
        top: 45%;
        left: 50%;
        transform: translate(-50%, -50%);
        font-size: 45px;
    }

    .news1 {
        width: 70%;
        position: relative;
        top: 550px;
        left: 0;
        line-height: 15px;
    }

    .news1 p {
        width: 90%;
        font-size: 12px;
        position: relative;
        left: 5px;
    }

    .news2 {
        width: 30%;
    }

    /* about */

    #about {
        height: 500px;
        width: 100%;
        background-color: #000;
    }

    .mission-img img {
        width: 35%;
        height: 20%;
        top: 450px;
        left: 60%;
    }

    .mission-title {
        font-size: 26px;
        line-height: 38px;
        position: relative;
        margin-top: 150px;
        left: 15%;
    }

    .mission-text {
        position: relative;
        top: 30px;
        left: 15%;
        margin: 20px 0;
        font-size: 14px;
        line-height: 20px;
    }


    .link {
        padding: 8px 30px;
        font-size: 16px;
        position: relative;
        left: 15%;
    }



    /* service */

    /*servicecard1*/

    #service-desktop {
        display: none;
    }

    .service-wrap {
        display: block;
        margin: 50px 5%;
    }
    .service-card {
        width: 100%;
        height: auto;
        color: black;
        background-color: white;
        transition: 0.3s;
        top: 50px;
        margin: 100px 0;
        padding: 0 0 50px;
    }

    .service-card h2 {
        margin-top: 50px;
        margin-left: 10%;
        font-size: 18px;
        font-weight: bold;
    }

    .sub {
        margin-top: 20px;
        margin-left: 10%;
    }

    .des {
        margin-top: 20px;
        margin-left: 10%;
        width: 80%;
        line-height: 25px;
    }

    .s-button {
        padding: 10px 25px;
        font-size: 14px;
        color: black;
        background-color: white;
        text-decoration: none;
        cursor: pointer;
        border: 1px #000000 solid;
        transition: 0.4s;
        display: inline-block;
        margin-top: 50px;
        margin-left: 45%;
    }

    .service-img {
        width: 100%;
        height: auto;
        top: -10px;
    }
    #service {
        padding: 10px 0 50px;
    }


    /* company */
    #company {
        padding: 30px 0;
    }
    .f-contein {
        display: block;
    }

    .overview {
        width: 100%;
        height: 200px;
    }

    .photo2 img {
        height: 200px;
    }

    .recruit {
        width: 100%;
        height: 200px;
    }

    .photo3 img {
        height: 200px;
    }

    .text h2 {
        font-size: 24px;
    }

    .text p {
        font-size: 18px;
    }

    .FAQ {
        width: 95%;
        margin: 25px 2.5% 0;
    }

    .FAQ h2 {
        left: 25%;
    }

    /* contact */
    #contact {
        padding: 10px 0;
    }

    .texts {
        margin: 10%;
    }

    #contact h3 {
        margin-top: -20px;
    }

    #contact .large-p {
        font-size: 34px;
        padding: 20px 0;
        line-height: 38px;
    }

    #contact p {
        font-size: 15px;
        line-height: 22px;
    }

    .link-contact {
        left: 50%;
        margin: 40px 0;
        padding: 10px 20px;
    }
    /* footer-logo */
    .footer-logo  {
        color: #ffffff;
        background-color: #000;
        text-align: center;
        font-weight: bold;
        font-size: 20px;
        line-height: 34px;
    }

    #footer-head {
        padding: 0 35%;
        display: flex;
        background-color: #000;
    }

}

</style>
