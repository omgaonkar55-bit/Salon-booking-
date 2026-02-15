‎<!DOCTYPE html>
‎<html lang="en">
‎<head>
‎<meta charset="UTF-8">
‎<title>Smart Salon – Appointment</title>
‎<meta name="viewport" content="width=device-width, initial-scale=1.0">
‎
‎<style>
‎body{
‎margin:0;
‎font-family:Arial, sans-serif;
‎background:#f5f5f5;
‎}
‎
‎.container{
‎max-width:420px;
‎margin:auto;
‎background:white;
‎padding:20px;
‎min-height:100vh;
‎}
‎
‎h1{
‎text-align:center;
‎color:#222;
‎}
‎
‎p{
‎text-align:center;
‎color:#666;
‎font-size:14px;
‎}
‎
‎input,select,button{
‎width:100%;
‎padding:12px;
‎margin-top:12px;
‎border-radius:6px;
‎border:1px solid #ccc;
‎font-size:15px;
‎}
‎
‎button{
‎background:#000;
‎color:white;
‎border:none;
‎cursor:pointer;
‎}
‎
‎.footer{
‎text-align:center;
‎margin-top:25px;
‎font-size:12px;
‎color:#999;
‎}
‎</style>
‎</head>
‎
‎<body>
‎
‎<div class="container">
‎
‎<h1>Smart Salon</h1>
‎<p>Book your haircut in 30 seconds</p>
‎
‎<form id="bookingForm">
‎
‎<input type="text" id="name" placeholder="Your Name" required>
‎
‎<input type="tel" id="phone" placeholder="Mobile Number" required>
‎
‎<select id="service" required>
‎<option value="">Select Service</option>
‎<option>Haircut</option>
‎<option>Beard Trim</option>
‎<option>Hair Spa</option>
‎<option>Facial</option>
‎</select>
‎
‎<input type="date" id="date" required>
‎
‎<input type="time" id="time" required>
‎
‎<button type="submit">Book Appointment</button>
‎
‎</form>
‎
‎<div class="footer">
‎Powered by your smartphone
‎</div>
‎
‎</div>
‎
‎<script>
‎document.getElementById("bookingForm").addEventListener("submit",function(e){
‎e.preventDefault();
‎
‎var name = document.getElementById("name").value;
‎var phone = document.getElementById("phone").value;
‎var service = document.getElementById("service").value;
‎var date = document.getElementById("date").value;
‎var time = document.getElementById("time").value;
‎
‎/* 👇 Salon WhatsApp number yaha change karo */
‎var salonNumber = "919860266589";
‎
‎var message =
‎"New Appointment Request%0A" +
‎"Name: " + name + "%0A" +
‎"Phone: " + phone + "%0A" +
‎"Service: " + service + "%0A" +
‎"Date: " + date + "%0A" +
‎"Time: " + time;
‎
‎var url = "https://wa.me/" + salonNumber + "?text=" + message;
‎
‎window.open(url, "_blank");
‎});
‎</script>
‎
‎</body>
‎</html>
‎
