# index.html<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Affinity Check - Bangui Edition</title>
    <style>
        :root { --primary: #ff4d6d; --bg: #0a0a0a; }
        body { font-family: sans-serif; background: var(--bg); color: white; display: flex; justify-content: center; align-items: center; height: 100vh; margin: 0; }
        .card { background: #1a1a1a; padding: 25px; border-radius: 20px; text-align: center; width: 85%; max-width: 350px; border: 1px solid #333; box-shadow: 0 10px 30px rgba(0,0,0,0.8); }
        h1 { color: var(--primary); font-size: 22px; margin-bottom: 20px; }
        input { width: 100%; padding: 12px; margin: 8px 0; border-radius: 10px; border: 1px solid #444; background: #252525; color: white; text-align: center; box-sizing: border-box; }
        button { background: var(--primary); color: white; border: none; padding: 15px; border-radius: 10px; width: 100%; font-weight: bold; margin-top: 10px; cursor: pointer; }
        #result-box { margin-top: 20px; display: none; padding: 15px; border-radius: 10px; animation: fadeIn 0.4s; }
        .vane { color: #ffcc00; font-size: 14px; line-height: 1.4; }
        .love { color: #00ffcc; font-weight: bold; font-size: 18px; text-shadow: 0 0 10px #00ffcc; }
        @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }
    </style>
</head>
<body>

<div class="card">
    <h1>✨ Destin & Affinités ✨</h1>
    <input type="text" id="n1" placeholder="Ton prénom">
    <input type="text" id="n2" placeholder="Prénom du crush">
    <button onclick="tester()">VOIR LE SCORE</button>
    <div id="result-box">
        <div id="score" style="font-size: 40px; font-weight: bold; margin-bottom: 10px;"></div>
        <div id="msg"></div>
    </div>
</div>

<script>
    function tester() {
        const p1 = document.getElementById('n1').value.trim().toLowerCase();
        const p2 = document.getElementById('n2').value.trim().toLowerCase();
        const res = document.getElementById('result-box');
        const sc = document.getElementById('score');
        const ms = document.getElementById('msg');

        if(!p1 || !p2) return alert("Mets les deux noms !");
        res.style.display = "block";

        // LE SEUL VRAI MATCH : PHARELL & ARIANA
        if ((p1 === "pharell" && p
        
