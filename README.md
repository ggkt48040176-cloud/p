# p
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>플라스틱 오염 환경 플랫폼</title>

    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: #f5f5f5;
            color: #333;
            scroll-behavior: smooth;
        }

        /* 메인 화면 */
        .main {
            height: 100vh;
            background: url('https://images.unsplash.com/photo-1508182311256-e3f7d5b69663?auto=format&fit=crop&w=1200&q=80') center/cover no-repeat;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: white;
            padding: 0 20px;
        }
        .main h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 6px rgba(0,0,0,0.7);
        }
        .scroll-btn {
            margin-top: 20px;
            background: rgba(255,255,255,0.8);
            padding: 12px 25px;
            border-radius: 20px;
            cursor: pointer;
            font-weight: bold;
        }

        /* 공통 섹션 */
        section {
            padding: 80px 10%;
        }
        h2 {
            font-size: 2rem;
            margin-bottom: 20px;
        }
        p {
            line-height: 1.6;
        }

        /* 카드 */
        .card-container {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
        }
        .card {
            flex: 1;
            min-width: 260px;
            background: white;
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }

        /* 인터랙션 */
        .interaction-box {
            margin-top: 20px;
            padding: 20px;
            background: #ffffff;
            border-radius: 12px;
            box-shadow: 0 2px 6px rgba(0,0,0,0.1);
            max-width: 400px;
        }

        #result {
            margin-top: 10px;
            font-weight: bold;
            color: #0066cc;
        }
    </style>
</head>

<body>

    <!-- 메인 화면 -->
    <div class="main">
        <h1>지구와 우리를 위한 작은 행동의 필수</h1>
        <div class="scroll-btn" onclick="document.getElementById('problem').scrollIntoView()">시작하기</div>
    </div>

    <!-- 섹션 1: 문제 이해 -->
    <section id="problem">
        <h2>플라스틱 오염 문제 이해하기</h2>
        <p>우리가 사용한 플라스틱은 대부분 자연에서 분해되지 않고, 미세플라스틱이 되어 다시 생태계로 돌아오고 있다.</p>
        <p><strong>“우리가 버린 플라스틱은 사라지지 않고 생태계로 되돌아온다.”</strong></p>

        <div class="card-container">
            <div class="card">
                <h3>전 세계 플라스틱 폐기량</h3>
                <p>매년 약 4억 톤 이상의 플라스틱이 생산된다.</p>
            </div>
            <div class="card">
                <h3>미세플라스틱 확산</h3>
                <p>대양, 토양, 대기까지 미세플라스틱이 검출된다.</p>
            </div>
        </div>
    </section>

    <!-- 섹션 2: 해결 아이디어 -->
    <section id="solution">
        <h2>과학적 해결 아이디어 소개</h2>
        <p>미생물과 효소는 플라스틱을 분자 단위로 분해할 수 있는 가능성을 가진다.</p>
        <p><strong>“과학은 플라스틱 문제를 분자 수준에서 해결하려고 한다.”</strong></p>

        <div class="card-container">
            <div class="card">
                <h3>PETase 효소</h3>
                <p>플라스틱 PET를 절단하는 능력을 가진 효소.</p>
            </div>
            <div class="card">
                <h3>미생물 재활용</h3>
                <p>분해된 단량체를 새로운 자원으로 전환 가능.</p>
            </div>
        </div>
    </section>

    <!-- 섹션 3: 인터랙션 -->
    <section id="interaction">
        <h2>인터랙션: 환경 조건에 따른 플라스틱 분해 속도</h2>
        <p>온도와 습도에 따라 분해 속도가 어떻게 달라지는지 직접 확인해보세요.</p>

        <div class="interaction-box">
            <label>온도 (°C)</label>
            <input type="range" id="temp" min="10" max="60" value="30" oninput="updateRate()">

            <label>습도 (%)</label>
            <input type="range" id="humidity" min="10" max="100" value="50" oninput="updateRate()">

            <p id="result">예상 분해 속도: 보통</p>
        </div>
    </section>

    <!-- 섹션 4: 행동 제안 -->
    <section id="action">
        <h2>일상에서 실천할 수 있는 행동</h2>
        <div class="card-container">
            <div class="card">
                <h3>하나, 일회용 줄이기</h3>
                <p>텀블러·장바구니 사용하기</p>
            </div>
            <div class="card">
                <h3>둘, 올바른 분리배출</h3>
                <p>깨끗하게 비우고 분리</p>
            </div>
            <div class="card">
                <h3>셋, 플라스틱 적게 사기</h3>
                <p>리필 스테이션 또는 무포장 제품 선택</p>
            </div>
        </div>
    </section>

    <!-- 섹션 5: 제작 의도 -->
    <section id="about">
        <h2>프로젝트 소개 및 제작 의도</h2>
        <p>생명과학·화학 전공 관심을 바탕으로, 플라스틱 문제를 과학적으로 이해하고 쉽게 설명하는 교육용 웹페이지를 제작하였다.</p>
        <p>복잡한 개념을 누구나 이해할 수 있는 방식으로 시각화하는 것이 가장 큰 도전이었다.</p>
    </section>

    <script>
        function updateRate() {
            let temp = document.getElementById("temp").value;
            let humidity = document.getElementById("humidity").value;
            let result = document.getElementById("result");

            if (temp > 45 && humidity > 70) {
                result.innerText = "예상 분해 속도: 매우 빠름";
            } else if (temp > 30 && humidity > 50) {
                result.innerText = "예상 분해 속도: 빠름";
            } else if (temp > 20) {
                result.innerText = "예상 분해 속도: 보통";
            } else {
                result.innerText = "예상 분해 속도: 느림";
            }
        }
    </script>

</body>
</html>
