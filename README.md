<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>احجز رحلتك لدهب</title>

<style>
body {
    font-family: Arial;
    margin: 0;
    background: #f5f5f5;
    text-align: center;
}

/* Hero */
.hero {
    background: linear-gradient(to right, #0077b6, #ff7b00);
    color: white;
    padding: 60px 20px;
}

.hero h1 {
    font-size: 30px;
}

/* Countdown */
.countdown {
    font-size: 24px;
    color: red;
    margin: 20px;
}

/* Form */
.form-box {
    background: white;
    padding: 20px;
    margin: 20px auto;
    width: 90%;
    max-width: 400px;
    border-radius: 10px;
    box-shadow: 0 0 10px #ccc;
}

input {
    width: 90%;
    padding: 10px;
    margin: 10px 0;
}

button {
    background: #27ae60;
    color: white;
    padding: 12px;
    border: none;
    width: 95%;
    border-radius: 5px;
    cursor: pointer;
}

/* WhatsApp */
.whatsapp {
    position: fixed;
    bottom: 20px;
    right: 20px;
    background: #25d366;
    color: white;
    padding: 15px;
    border-radius: 50%;
    text-decoration: none;
}
</style>

</head>

<body>

<div class="hero">
    <h1>🔥 مغامرة دهب مستنياك</h1>
    <p>احجز قبل ما الأماكن تخلص!</p>
</div>

<div class="countdown" id="countdown"></div>

<div class="form-box">
    <h2>احجز الآن</h2>
    <input type="text" placeholder="اسمك">
    <input type="email" placeholder="الإيميل">
    <input type="tel" placeholder="رقم الموبايل">
    <button onclick="alert('تم الحجز بنجاح!')">تأكيد الحجز</button>
</div>

<a class="whatsapp" href="https://wa.me/201XXXXXXXXX" target="_blank">
💬
</a>

<script>
// Deadline
var countDownDate = new Date("May 5, 2026 23:59:59").getTime();

var x = setInterval(function() {
    var now = new Date().getTime();
    var distance = countDownDate - now;

    var days = Math.floor(distance / (1000 * 60 * 60 * 24));
    var hours = Math.floor((distance % (1000*60*60*24)) / (1000*60*60));
    var minutes = Math.floor((distance % (1000*60*60)) / (1000*60));

    document.getElementById("countdown").innerHTML =
    "⏳ متبقي " + days + " يوم " + hours + " ساعة " + minutes + " دقيقة";

    if (distance < 0) {
        clearInterval(x);
        document.getElementById("countdown").innerHTML = "❌ انتهى الحجز";
    }
}, 1000);
</script>

</body>
</html>
