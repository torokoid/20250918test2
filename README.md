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
<!-- ヘッダー -->
<header>
  <a href="index.html" class="team-logo">
    <img src="team-logo.svg" alt="swim experience のロゴ">
  </a>
</header>

<!-- ヒーロー -->
<section class="hero">
  <h2>Life is short, so I want to swim faster.</h2>
  <small>人生は短いらしい。そうなら速く泳ぎたい</small>
  <img src="down.png" alt="プールの底画像">
</section>

<!-- ボディ -->
<main>
  <!-- 流れ文字 -->
  <h1 class="white">
    <marquee behavior="scroll" direction="left">
      スイム・イクスピリエンスとは 【競泳を体験・実感する】の意味です。
      選手の理想通りに、上手く、速くなる実感を持つサポートをいたします。
    </marquee>
  </h1>

  <!-- 活動内容 -->
  <section>
    <h2>スイム・イクスピリエンスの活動と内容</h2>
    <ul>
      <li>2025年7月から準備し、2026年より本格活動を計画中。</li>
      <li>現在の活動は「①競泳選手傾向診断」「②レース動画解析」の２つのみ活動中。</li>
    </ul>
    <p>その他の活動は準備が整い次第、発信します。</p>
  </section>

  <!-- お問い合わせフォーム -->
  <section>
    <h4>お問い合わせ先</h4>
    <form action="mailform.php" method="post">
      <p>お名前: <input type="text" name="name" id="name" required></p>
      <p>性別:
        <input type="radio" name="sex" value="男" required> 男
        <input type="radio" name="sex" value="女" required> 女
      </p>
      <p>メールアドレス: <input type="email" name="email" required></p>
      <p>メッセージ</p>
      <textarea name="message" rows="5" required></textarea>
      <p><input type="submit" value="送信する"></p>
    </form>
  </section>
</main>

<!-- フッター -->
<footer>
  <a href="index.html" class="team-logo">
    <img src="team-logo.svg" alt="swim experience のロゴ">
  </a>
  <p class="copyright">&copy; 2025/07/14 Y. Omori</p>
</footer>

</body>
</html>

