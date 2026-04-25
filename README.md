.
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>نظام الكلية الحربية</title>
    <style>
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; background: linear-gradient(135deg, #0f2027, #203a43, #2c5364); color: #fff; display: flex; justify-content: center; align-items: center; height: 100vh; margin: 0; }
        .container { background: rgba(0, 0, 0, 0.8); padding: 25px; border-radius: 15px; box-shadow: 0 10px 30px rgba(0,0,0,0.5); text-align: center; width: 90%; max-width: 400px; border: 2px solid #ffd700; }
        input { width: 80%; padding: 12px; margin: 15px 0; border-radius: 5px; border: none; text-align: center; }
        .btn { background: #ffd700; color: #000; padding: 12px 20px; border: none; border-radius: 5px; font-weight: bold; cursor: pointer; width: 85%; }
        .output { margin-top: 20px; padding: 15px; background: rgba(255,255,255,0.1); border-radius: 10px; min-height: 50px; }
        .rank { color: #ffd700; font-weight: bold; font-size: 1.2em; display: block; }
        .footer { margin-top: 20px; font-size: 0.8em; border-top: 1px solid #444; padding-top: 10px; }
    </style>
</head>
<body>
    <div class="container">
        <h2>الكلية الحربية</h2>
        <input type="text" id="nameInput" placeholder="أدخل اسمك هنا...">
        <button class="btn" onclick="welcome()">دخول النظام</button>
        <div class="output" id="result">بانتظار إدخال الاسم...</div>
        <div class="footer">وطن لا نحميه لا نستحق العيش فيه<br><strong>هندسة وتصميم رضوان الوريفي</strong></div>
    </div>
    <script>
        function welcome() {
            let name = document.getElementById("nameInput").value.trim();
            let res = document.getElementById("result");
            if (name === "") { res.innerHTML = "يرجى كتابة الاسم"; return; }
            if (name.includes("محمد المليكي") || name.includes("خالد المليكي")) { res.innerHTML = "<span class='rank'>الرتبة: لواء</span> مرحباً بكم بالكلية الحربية"; } 
            else if (name.includes("محمد الحاتمي")) { res.innerHTML = "<span class='rank'>الرتبة: دكتور</span> مشرفنا يا دكتور محمد"; }
            else if (name.includes("مكرم الحاتمي")) { res.innerHTML = "<span class='rank'>الرتبة: جنرال</span> مرحباً بك يا قائد"; }
            else if (name.includes("نصر الحاتمي")) { res.innerHTML = "<span class='rank'>الرتبة: رائد</span> أهلاً بك يا نصر"; }
            else if (name.includes("حاتم الحاتمي")) { res.innerHTML = "<span class='rank'>الرتبة: ملازم أول</span> مرحباً يا حاتم"; }
            else if (name.includes("رضوان الوريفي")) { res.innerHTML = "<span class='rank'>الرتبة: مهندس</span> أهلاً بمصمم النظام"; }
            else { res.innerHTML = "مرحباً بك يا " + name + " في الكلية الحربية"; }
        }
    </script>
</body>
</html>