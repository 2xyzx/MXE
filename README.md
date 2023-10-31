# MXE
mbti와 에니어그램 자판기

<!DOCTYPE html>
<html>
<head>
    <title>Random Generator</title>
    <script type="text/javascript">
        function generateRandomValues() {
            // A 배열에 1부터 16까지의 난수 저장
            var A = [];
            for (var i = 0; i < 16; i++) {
                A.push(Math.floor(Math.random() * 16) + 1);
            }

            // B 배열에 1부터 8까지의 난수 저장
            var B = [];
            for (var i = 0; i < 8; i++) {
                B.push(Math.floor(Math.random() * 8) + 1);
            }

            // C 배열에 1부터 18까지의 난수 저장
            var C = [];
            for (var i = 0; i < 18; i++) {
                C.push(Math.floor(Math.random() * 18) + 1);
            }

            // D 배열에 1부터 6까지의 난수 저장
            var D = [];
            for (var i = 0; i < 6; i++) {
                D.push(Math.floor(Math.random() * 6) + 1);
            }

            var MBTI = ["ISTJ", "ISFJ", "ESTP", "ESFP", "INTJ", "INFJ", "ENTP", "ENFP",
            "ISTP", "INTP", "ESTJ", "ENTJ", "ISFP", "INFP", "ESFJ", "ENFJ"];
            var CogDev = ["l---", "ll--", "l-l-", "l--l", "lll-", "ll-l", "l-ll", "llll"];
            var Enneagram = ["1w2", "1w9", "8w7", "8w9", "9w1", "9w8",
            "2w1", "2w3", "3w2", "3w4", "4w3", "4w5",
            "5w4", "5w6", "6w5", "6w7", "7w6", "7w8"];
            var EnneaGut = ["1w2", "1w9", "8w7", "8w9", "9w1", "9w8"];
            var EnneaHeart = ["2w1", "2w3", "3w2", "3w4", "4w3", "4w5"];
            var EnneaHead = ["5w4", "5w6", "6w5", "6w7", "7w6", "7w8"];
            var EnneaSub = ["sp/so", "sp/sx", "so/sp", "so/sx", "sx/sp", "sx/so"];

            var randomIndexMBTI = Math.floor(Math.random() * 16);
            var randomIndexCogDev = Math.floor(Math.random() * 8);
            var randomIndexEnneagram = Math.floor(Math.random() * 18);
            var randomIndexEnneaSub = Math.floor(Math.random() * 6);

            document.getElementById("resultMBTI").textContent = "MBTI: " + MBTI[randomIndexMBTI];
            document.getElementById("resultCogDev").textContent = "기능 개발: " + CogDev[randomIndexCogDev];
            document.getElementById("resultEnneagram").textContent = "에니어그램: " + Enneagram[randomIndexEnneagram];
            document.getElementById("resultEnneaSub").textContent = "하위 유형: " + EnneaSub[randomIndexEnneaSub];
        }
    </script>
</head>
<body>
    <h1>MBTI X Enneagram 조합 자판기</h1>
    <button onclick="generateRandomValues()">유형 뽑기</button>
    <p id="resultMBTI"></p>
    <p id="resultCogDev"></p>
    <p id="resultEnneagram"></p>
    <p id="resultEnneaSub"></p>
</body>
</html>
