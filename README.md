#SWIM EXPERIENCE HOME PAGE
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>世界時計付きページ</title>
  <style>
    /* ------------------------------
       ヘッダー
    ------------------------------ */
    .header {
      width: 960px;
      height: 170px;
      margin: 0 auto;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .header .logo img {
      display: block;
      height: 60px;
    }

    /* ------------------------------
       ヒーロー
    ------------------------------ */
    .hero {
      width: 100%;
      height: 350px;
      display: flex;
      justify-content: center;
      align-items: center;
      background-image: url("down.png");
      background-repeat: no-repeat;
      background-size: cover;
      background-position: center center;
      background-attachment: fixed;
      color: #fff;
      font-size: 48px;
      line-height: 1.2;
      text-align: center;
      margin: 100px 0 40px 0;
      flex-direction: column;
      position: relative;
    }
    .hero h2 {
      font-size: 48px;
      font-weight: 700;
    }
    .hero a {
      display: grid;
      place-items: center;
      width: 60px;
      height: 60px;
      background-color: #6a9631;
      border-radius: 50%;
      box-shadow: 0px 12px 20px rgba(0, 0, 0, 0.1);
      position: absolute;
      left: 50%;
      bottom: 0;
      transform: translate(-50%, 50%);
    }
    .hero a img {
      width: 24px;
      height: 24px;
    }

    /* ------------------------------
       点滅エフェクト
    ------------------------------ */
    .blinking {
      animation: blink 1.5s ease-in-out infinite alternate;
    }
    @keyframes blink {
      0% { opacity: 0; }
      100% { opacity: 1; }
    }

    /* ------------------------------
       背景
    ------------------------------ */
    body::before {
      content: "";
      display: block;
      position: fixed;
      top: 0;
      left: 0;
      z-index: -1;
      width: 100%;
      height: 100vh;
      background: url("haikei.JPG") center/cover no-repeat;
    }

    /* ------------------------------
       ナビゲーション
    ------------------------------ */
    .nav {
      color: #fff;
      text-align: center;
      height: 200px;
      background-image: url("../img/hero-background.jpg");
      background-size: cover;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      position: relative;
    }
    .nav h2 {
      font-size: 48px;
      font-weight: 700;
    }
    .nav p {
      font-size: 20px;
      font-weight: 400;
      margin-top: 20px;
    }

    /* ------------------------------
       ボタン
    ------------------------------ */
    .button {
      display: inline-block;
      color: #fff;
      background-color: #06f;
      padding: 1em 2em;
      border-radius: 8px;
      text-decoration: none;
    }

    /* ------------------------------
       フッター
    ------------------------------ */
    #footer2-parts * { margin: 0; padding: 0; }
    #footer2-parts ul { list-style: none; }

    #footer2-parts {
      background: #eee;
      color: #555;
      padding: 2rem;
    }
    #footer2-parts .footer2-1-parts {
      flex: 1;
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }
    #footer2-parts small {
      display: block;
      text-align: right;
      margin-top: 2rem;
    }

    /* SNSアイコン */
    .sns1-parts {
      list-style: none;
      margin: 0;
      padding: 0;
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
    }
    .sns1-parts i {
      font-size: 30px;
    }

    /* ------------------------------
       Google Map
    ------------------------------ */
    .iframe-box1-parts {
      width: 100%;
      height: 0;
      padding-top: 56.25% !important;
      position: relative;
      overflow: hidden;
    }
    .iframe-box1-parts iframe {
      position: absolute;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
    }

    /* ------------------------------
       テーブル
    ------------------------------ */
    .week2-parts {
      width: 100%;
      border-collapse: separate;
      border-spacing: 0;
      border-radius: 10px;
      border: 1px solid #ccc;
      table-layout: fixed;
      background: #fff;
      color: #555;
    }
    .week2-parts th,
    .week2-parts td {
      padding: 1rem 0;
      text-align: center;
      border-bottom: 1px solid #ccc;
      border-right: 1px solid #ccc;
    }
    .week2-parts th {
      background: #fafafa;
    }
    .week2-parts th:last-child,
    .week2-parts td:last-child {
      border-right: none;
    }
    .week2-parts tr:last-child td {
      border-bottom: none;
    }

    /* ------------------------------
       リストカード
    ------------------------------ */
    .list-normal3-parts .list-parts {
      position: relative;
      overflow: hidden;
      padding: 1.5rem;
      background: #fff;
      color: #555;
      border: 1px solid #ccc;
      margin-bottom: 2rem;
    }
    .list-normal3-parts .list-parts h4 {
      font-size: 1.3rem;
      margin-bottom: 0.5rem;
    }
    .list-normal3-parts .list-parts p {
      font-size: 0.9rem;
      line-height: 1.6;
    }
    .list-normal3-parts .icon-bg1-parts {
      background: #ff3535;
      color: #fff;
      position: absolute;
      top: 0;
      left: 0;
      font-size: 0.7rem;
      transform: rotate(-45deg) translate(-2.4rem, -3rem);
      width: 10rem;
      text-align: center;
    }
    .list-normal3-parts .icon-bg2-parts {
      background: #358bff;
      color: #fff;
      position: absolute;
      top: 0;
      left: 0;
      font-size: 0.7rem;
      transform: rotate(-45deg) translate(-2.4rem, -3rem);
      width: 10rem;
      text-align: center;
    }

    /* ------------------------------
       レスポンシブ
    ------------------------------ */
    @media screen and (min-width: 500px) {
      .list-normal3-parts .list-parts {
        display: flex;
        gap: 1.5rem;
      }
      .list-normal3-parts .list-parts figure {
        width: 30%;
      }
    }
    @media screen and (min-width: 700px) {
      #footer2-parts {
        display: flex;
        gap: 2rem;
      }
      #footer2-parts .footer2-1-parts {
        text-align: left;
        width: 40%;
      }
    }
  </style>
</head>
<body>

  <header class="header">
    <div class="logo"><img src="logo.png" alt="Logo"></div>
  </header>

  <section class="hero">
    <h2 class="blinking">世界時計</h2>
    <p>リアルタイムで各都市の時刻を表示</p>
  </section>

  <!-- ここに Python で生成した時刻表を iframe で埋め込み or JS で生成可能 -->
  <div style="max-width:800px;margin:0 auto;">
    <table class="week2-parts">
      <thead>
        <tr><th>都市</th><th>時刻</th></tr>
      </thead>
      <tbody id="world-clock">
        <tr><td>Tokyo</td><td>2025-10-01 09:30:00</td></tr>
        <tr><td>Bangkok</td><td>2025-10-01 07:30:00</td></tr>
        <tr><td>Berlin</td><td>2025-10-01 03:30:00</td></tr>
      </tbody>
    </table>
  </div>

  <footer id="footer2-parts">
    <div class="footer2-1-parts">
      <p>© 2025 世界時計サンプル</p>
    </div>
  </footer>

</body>
</html>

