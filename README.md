<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>텍스트 복사 버튼</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f4f4f4;
        }
        .container {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            border: none;
            border-radius: 5px;
            background-color: #007bff;
            color: white;
            cursor: pointer;
            margin-top: 10px;
        }
        button:hover {
            background-color: #0056b3;
        }
    </style>
    <script>
        function copyText() {
            const text = "#위대한뮤지션100인전#이랜드뮤지엄#현대백화점무역센터점";
            navigator.clipboard.writeText(text).then(() => {
                alert("텍스트가 복사되었습니다!\n붙여넣기(Ctrl+V 또는 Cmd+V) 하세요.");
            }).catch(err => {
                console.error("복사 실패: ", err);
            });
        }
    </script>
</head>
<body>
    <div class="container">
        <h2>텍스트 복사</h2>
        <p>아래 버튼을 눌러 텍스트를 복사하세요.</p>
        <button onclick="copyText()">📋 텍스트 복사</button>
    </div>
</body>
</html>
