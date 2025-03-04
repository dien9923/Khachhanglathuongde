<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Đánh giá 5 sao - Dương Nhật</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 50px;
        }
        .stars {
            font-size: 50px;
            cursor: pointer;
        }
        .star {
            color: gray;
        }
        .star.selected {
            color: gold;
        }
        #result {
            font-size: 24px;
            margin-top: 10px;
        }
    </style>
</head>
<body>

    <h1>Đánh giá của Dương Nhật</h1>
    <div class="stars" id="starContainer">
        <span class="star" data-value="1">★</span>
        <span class="star" data-value="2">★</span>
        <span class="star" data-value="3">★</span>
        <span class="star" data-value="4">★</span>
        <span class="star" data-value="5">★</span>
    </div>
    <p id="result">Bấm vào để đánh giá!</p>

    <script>
        const stars = document.querySelectorAll('.star');
        const result = document.getElementById('result');

        stars.forEach(star => {
            star.addEventListener('click', function() {
                // Luôn đánh giá 5 sao dù bấm vào sao nào
                stars.forEach(s => s.classList.add('selected'));
                result.innerText = "Cảm ơn bạn! Bạn đã đánh giá 5 sao!";
            });
        });
    </script>

</body>
</html>
