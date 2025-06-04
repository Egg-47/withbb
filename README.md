# withbb
<!DOCTYPE html>
<html lang="zh">
<head>
  <meta charset="UTF-8">
  <title>我们的恋爱记录</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      margin: 0;
      font-family: 'Arial', sans-serif;
      background-color: #fafafa;
      color: #444;
    }

    header {
      text-align: center;
      background-color: #ffe4e9;
      padding: 30px;
    }

    header h1 {
      color: #e66a8d;
      font-size: 2.5em;
    }

    /* 顶部轮播图 */
    .carousel {
      overflow: hidden;
      position: relative;
      background-color: #fff;
    }

    .carousel-track {
      display: flex;
      animation: scrollLeft 20s linear infinite;
    }

    .carousel img {
      height: 300px;
      width: auto;
      margin-right: 10px;
      border-radius: 12px;
    }

    @keyframes scrollLeft {
      0% { transform: translateX(0); }
      100% { transform: translateX(-50%); }
    }

    /* 内容区块 */
    .section {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      align-items: center;
      max-width: 1000px;
      margin: 40px auto;
      padding: 20px;
      background: #fff;
      border-radius: 16px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.08);
    }

    .section:nth-child(even) {
      flex-direction: row-reverse;
      background-color: #fef5f7;
    }

    .section img {
      width: 90%;
      max-width: 400px;
      border-radius: 16px;
      object-fit: cover;
    }

    .section .text {
      flex: 1 1 300px;
      padding: 20px;
    }

    .section h2 {
      color: #e66a8d;
    }

    .section p {
      line-height: 1.6;
    }

    /* 音乐切换按钮 */
    .music-controls {
      text-align: center;
      margin: 20px 0;
    }

    .music-controls button {
      margin: 5px;
      padding: 10px 20px;
      background-color: #e66a8d;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }

    .music-controls button:hover {
      background-color: #d05576;
    }

    /* 响应式布局 */
    @media (max-width: 768px) {
      .section {
        flex-direction: column !important;
        text-align: center;
      }

      .section img, .section .text {
        width: 100%;
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>我们的恋爱记录</h1>
    <p>珍藏每一个特别的瞬间</p>
  </header>

  <!-- 顶部轮播图 -->
  <div class="carousel">
    <div class="carousel-track">
      <img src="https://via.placeholder.com/400x300?text=特别瞬间1">
      <img src="https://via.placeholder.com/400x300?text=特别瞬间2">
      <img src="https://via.placeholder.com/400x300?text=特别瞬间3">
      <img src="https://via.placeholder.com/400x300?text=特别瞬间1">
      <img src="https://via.placeholder.com/400x300?text=特别瞬间2">
    </div>
  </div>

  <!-- 音乐播放器 -->
  <audio id="bg-music" autoplay loop>
    <source src="music1.mp3" type="audio/mpeg">
    您的浏览器不支持音频播放。
  </audio>

  <div class="music-controls">
    <button onclick="changeMusic('music1.mp3')">音乐1</button>
    <button onclick="changeMusic('music2.mp3')">音乐2</button>
    <button onclick="changeMusic('music3.mp3')">音乐3</button>
  </div>

  <!-- 图文区块 -->
  <div class="section">
    <img src="https://via.placeholder.com/400x300?text=初遇">
    <div class="text">
      <h2>第一次相遇</h2>
      <p>那天阳光正好，我们在人群中对视，笑容成为我们故事的开端。</p>
    </div>
  </div>

  <div class="section">
    <img src="https://via.placeholder.com/400x300?text=约会">
    <div class="text">
      <h2>第一次约会</h2>
      <p>在那家咖啡馆里，我们谈天说地，好像认识了很久。</p>
    </div>
  </div>

  <div class="section">
    <img src="https://via.placeholder.com/400x300?text=旅行">
    <div class="text">
      <h2>一起旅行</h2>
      <p>那次旅行是我们最自由的时光，每一张照片都藏着我们的快乐。</p>
    </div>
  </div>

  <script>
    function changeMusic(src) {
      const music = document.getElementById("bg-music");
      music.src = src;
      music.play();
    }
  </script>

</body>
</html>
