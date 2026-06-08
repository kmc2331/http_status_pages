<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<title>404 - Lost Duck</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    height:100vh;
    overflow:hidden;
    font-family:sans-serif;
    background:linear-gradient(
        180deg,
        #9ad7ff 0%,
        #6fc4ff 40%,
        #43a9ff 100%
    );
}

/* プールのタイル */

.pool{
    position:absolute;
    inset:0;

    background:
    repeating-linear-gradient(
        0deg,
        rgba(255,255,255,.25) 0px,
        rgba(255,255,255,.25) 2px,
        transparent 2px,
        transparent 60px
    ),

    repeating-linear-gradient(
        90deg,
        rgba(255,255,255,.25) 0px,
        rgba(255,255,255,.25) 2px,
        transparent 2px,
        transparent 60px
    );
}

/* 水面 */

.water{
    position:absolute;
    inset:0;

    background:
    radial-gradient(circle at 20% 20%,
    rgba(255,255,255,.35),
    transparent 40%),

    radial-gradient(circle at 80% 30%,
    rgba(255,255,255,.25),
    transparent 40%);

    animation:wave 6s ease-in-out infinite;
}

@keyframes wave{
    50%{
        transform:translateY(-8px);
    }
}

/* 404 */

.code{
    position:absolute;
    top:43%;
    left:50%;

    transform:translate(-50%,-50%);

    font-size:230px;
    font-weight:bold;

    color:rgba(255,255,255,.92);

    text-shadow:
    0 0 20px rgba(255,255,255,.6),
    0 0 40px rgba(0,0,0,.15);

    z-index:10;
}

/* メッセージ */

.message{
    position:absolute;

    left:50%;
    top:58%;

    transform:translateX(-50%);

    text-align:center;
    color:white;

    z-index:10;
}

.message h2{
    font-size:42px;
    margin-bottom:12px;
}

.message p{
    font-size:20px;
}

/* アヒル */

.duck{
    position:absolute;

    font-size:80px;

    animation:float 4s ease-in-out infinite;
}

@keyframes float{
    50%{
        transform:translateY(-15px);
    }
}

/* 配置 */

.d1{
    top:10%;
    left:12%;
}

.d2{
    top:18%;
    right:15%;
    animation-delay:1s;
}

.d3{
    top:42%;
    left:8%;
    animation-delay:2s;
}

.d4{
    top:35%;
    right:8%;
    animation-delay:.5s;
}

.d5{
    bottom:15%;
    left:18%;
    animation-delay:1.5s;
}

.d6{
    bottom:10%;
    right:20%;
    animation-delay:2.5s;
}

/* ボタン */

.button{
    position:absolute;

    left:50%;
    bottom:50px;

    transform:translateX(-50%);

    z-index:10;
}

.button a{
    text-decoration:none;

    color:#1670d0;
    background:white;

    padding:14px 34px;

    border-radius:30px;

    font-weight:bold;

    box-shadow:
    0 5px 20px rgba(0,0,0,.15);
}
</style>
</head>

<body>

<div class="pool"></div>
<div class="water"></div>

<div class="duck d1">🦆</div>
<div class="duck d2">🦆</div>
<div class="duck d3">🐥</div>
<div class="duck d4">🦆</div>
<div class="duck d5">🐥</div>
<div class="duck d6">🦆</div>

<div class="code">404</div>

<div class="message">
    <h2>ページが流されちゃったみたい...</h2>
    <p>探しているページはプールのどこかを漂っています。</p>
</div>

<div class="button">
    <a href="/">トップへ戻る</a>
</div>

</body>
</html>
