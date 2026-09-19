# Imka1
Imka fr1
<!DOCTYPE html>
<html lang="pl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Fikcyjna Karta DEMO</title>

<style>
* {
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

body {
    margin: 0;
    background: #eef1f5;
    color: #18202b;
}

.app {
    max-width: 430px;
    min-height: 100vh;
    margin: auto;
    background: #f7f8fa;
}

header {
    background: white;
    padding: 22px 20px 16px;
    border-bottom: 1px solid #ddd;
}

.logo {
    font-size: 24px;
    font-weight: 800;
}

.subtitle {
    color: #6b7280;
    margin-top: 5px;
}

.demo {
    margin: 16px;
    padding: 12px;
    text-align: center;
    background: #fff0f0;
    border: 2px solid #d32f2f;
    border-radius: 14px;
    color: #a71919;
    font-weight: 800;
}

.content {
    padding: 0 16px 30px;
}

.form {
    background: white;
    padding: 18px;
    border-radius: 18px;
    box-shadow: 0 3px 12px #00000012;
}

label {
    display: block;
    margin: 12px 0 6px;
    font-size: 13px;
    font-weight: bold;
}

input {
    width: 100%;
    padding: 13px;
    border: 1px solid #d5d9df;
    border-radius: 11px;
    font-size: 16px;
}

button {
    width: 100%;
    padding: 14px;
    margin-top: 18px;
    border: 0;
    border-radius: 12px;
    background: #c62828;
    color: white;
    font-size: 16px;
    font-weight: bold;
    cursor: pointer;
}

.card {
    margin-top: 18px;
    background: white;
    border-radius: 20px;
    overflow: hidden;
    box-shadow: 0 5px 18px #00000018;
}

.card-header {
    background: #222b36;
    color: white;
    padding: 18px;
}

.badge {
    display: inline-block;
    background: #e53935;
    padding: 5px 9px;
    border-radius: 7px;
    font-size: 12px;
    font-weight: bold;
    margin-bottom: 12px;
}

.title {
    font-size: 22px;
    font-weight: bold;
}

.card-body {
    padding: 20px;
}

.row {
    padding: 11px 0;
    border-bottom: 1px solid #edf0f2;
}

.row:last-child {
    border-bottom: 0;
}

.key {
    font-size: 11px;
    color: #737b86;
    margin-bottom: 4px;
}

.value {
    font-size: 17px;
    font-weight: bold;
}

.warning {
    margin: 0 20px 20px;
    padding: 12px;
    background: #fff1f1;
    color: #a71919;
    border-radius: 12px;
    text-align: center;
    font-size: 12px;
    font-weight: bold;
}
</style>
</head>

<body>

<div class="app">

<header>
    <div class="logo">Moja Karta</div>
    <div class="subtitle">Fikcyjna aplikacja demonstracyjna</div>
</header>

<div class="demo">
    DEMO • NIE JEST DOKUMENTEM TOŻSAMOŚCI
</div>

<div class="content">

<div class="form">

<label>Imię</label>
<input id="name" placeholder="Np. Jan">

<label>Nazwisko</label>
<input id="surname" placeholder="Np. Kowalski">

<label>Data urodzenia</label>
<input id="birth" placeholder="DD.MM.RRRR">

<label>Fikcyjny numer ID</label>
<input id="id" placeholder="Np. DEMO-123456">

<label>Imię matki</label>
<input id="mother" placeholder="Np. Anna">

<label>Imię ojca</label>
<input id="father" placeholder="Np. Piotr">

<label>Miejsce urodzenia</label>
<input id="place" placeholder="Np. Gdynia">

<label>Obywatelstwo</label>
<input id="citizenship" placeholder="Np. polskie">

<button onclick="generate()">
    Pokaż fikcyjną kartę
</button>

</div>

<div class="card">

<div class="card-header">
    <div class="badge">FIKCYJNE DEMO</div>
    <div class="title">Fikcyjna karta</div>
</div>

<div class="card-body">

<div class="row">
<div class="key">IMIĘ</div>
<div class="value" id="outName">---</div>
</div>

<div class="row">
<div class="key">NAZWISKO</div>
<div class="value" id="outSurname">---</div>
</div>

<div class="row">
<div class="key">DATA URODZENIA</div>
<div class="value" id="outBirth">---</div>
</div>

<div class="row">
<div class="key">FIKCYJNY NUMER ID</div>
<div class="value" id="outId">---</div>
</div>

<div class="row">
<div class="key">IMIĘ MATKI</div>
<div class="value" id="outMother">---</div>
</div>

<div class="row">
<div class="key">IMIĘ OJCA</div>
<div class="value" id="outFather">---</div>
</div>

<div class="row">
<div class="key">MIEJSCE URODZENIA</div>
<div class="value" id="outPlace">---</div>
</div>

<div class="row">
<div class="key">OBYWATELSTWO</div>
<div class="value" id="outCitizenship">---</div>
</div>

</div>

<div class="warning">
TO JEST WYŁĄCZNIE FIKCYJNE DEMO.<br>
NIE JEST DOKUMENTEM TOŻSAMOŚCI.
</div>

</div>

</div>
</div>

<script>
function get(id) {
    return document.getElementById(id).value || "---";
}

function generate() {
    document.getElementById("outName").textContent = get("name");
    document.getElementById("outSurname").textContent = get("surname");
    document.getElementById("outBirth").textContent = get("birth");
    document.getElementById("outId").textContent = get("id");
    document.getElementById("outMother").textContent = get("mother");
    document.getElementById("outFather").textContent = get("father");
    document.getElementById("outPlace").textContent = get("place");
    document.getElementById("outCitizenship").textContent = get("citizenship");
}
</script>

</body>
</html>


