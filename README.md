
<!DOCTYPE html>
<html>
<head>
<title>Сайт Андрея</title>
<style>
body {
font-family: Arial, sans-serif;
}
</style>
</head>
<body>
<h1>Сайт Андрея</h1>
<form id="register-form">
<label for="username">Имя пользователя:</label>
<input type="text" id="username" name="username"><br><br>
<label for="password">Пароль:</label>
<input type="password" id="password" name="password"><br><br>
<button id="register-button">Зарегистрироваться</button>
</form>
<p id="result"></p>

<script>
let users = [];

document.getElementById("register-button").addEventListener("click", function(event) {
event.preventDefault();
let username = document.getElementById("username").value;
let password = document.getElementById("password").value;
if (username && password) {
let user = {
username: username,
password: password
};
users.push(user);
document.getElementById("result").innerHTML = "Если ты это читаешь, то ты лох";
} else {
document.getElementById("result").innerHTML = "Введите имя пользователя и пароль";
}
});
</script>
</body>
</html>

