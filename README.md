# -
조랭의 모든 것
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>친구 소개</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }
    body {
      background-color: #f4f4f4;
      text-align: center;
    }
    .section {
      opacity: 0;
      transform: translateY(50px);
      transition: opacity 1s ease-out, transform 1s ease-out;
      padding: 100px 20px;
    }
    .section.visible {
      opacity: 1;
      transform: translateY(0);
    }
    .intro {
      background: #3498db;
      color: white;
      padding: 150px 20px;
      font-size: 24px;
    }
    .gallery img {
      width: 200px;
      margin: 10px;
      border-radius: 10px;
    }
  </style>
</head>
<body>
  <div class="section intro">
    <h1>내 친구를 소개합니다!</h1>
    <p>멋진 내 친구를 만나보세요.</p>
  </div>
  
  <div class="section">
    <h2>친구의 특징</h2>
    <p>항상 밝고 긍정적인 에너지를 가지고 있어요!</p>
  </div>
  
  <div class="section">
    <h2>취미와 관심사</h2>
    <p>음악 듣기, 여행, 맛있는 음식 먹기</p>
  </div>
  
  <div class="section gallery">
    <h2>사진 갤러리</h2>
    <img src="https://via.placeholder.com/200" alt="친구 사진 1">
    <img src="https://via.placeholder.com/200" alt="친구 사진 2">
  </div>
  
  <div class="section">
    <h2>추억 이야기</h2>
    <p>함께했던 멋진 순간들을 잊지 못해요!</p>
  </div>
  
  <script>
    document.addEventListener("DOMContentLoaded", () => {
      const sections = document.querySelectorAll(".section");
      
      const observer = new IntersectionObserver((entries, observer) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.classList.add("visible");
          }
        });
      }, { threshold: 0.3 });
      
      sections.forEach(section => {
        observer.observe(section);
      });
    });
  </script>
</body>
</html>
