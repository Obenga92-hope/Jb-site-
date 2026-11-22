# Jb-site-
Index_html

<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>JB - Smart Customer Care</title>
<style>
*{box-sizing:border-box}
body{margin:0;font-family:Arial,sans-serif;background:#080f25;color:white}
header{padding:20px;display:flex;justify-content:space-between;align-items:center;background:#080f25}
.logo{font-size:30px;font-weight:bold;color:white}
.logo span{color:#9365ff}
nav a{color:white;text-decoration:none;margin:8px;font-size:13px}
.hero{padding:65px 7%;background:linear-gradient(120deg,#101a39,#080f25)}
.tag{color:#a98aff;font-weight:bold}
h1{font-size:43px;line-height:1.15}
h1 span{color:#986cff}
p{line-height:1.7;color:#cbd2e5}
.btn{display:inline-block;background:#7546ed;color:white;padding:14px 22px;border-radius:25px;text-decoration:none;margin-top:15px}
.card{background:white;color:#111a35;border-radius:18px;padding:20px;margin-top:30px;max-width:430px}
.card h3{background:#6840e5;color:white;padding:15px;border-radius:12px;margin-top:0}
.message{padding:12px;background:#eeeafa;border-radius:12px;margin:12px 0;font-size:14px}
.user{background:#7045e9;color:white;text-align:right}
input{width:75%;padding:13px;border:1px solid #ddd;border-radius:20px}
button{padding:13px;background:#7045e9;color:white;border:0;border-radius:20px;cursor:pointer}
section.features{background:white;color:#111a35;padding:45px 7%;text-align:center}
.features h2{font-size:30px}
.feature{padding:20px;margin:12px;background:#f3f0ff;border-radius:15px}
footer{padding:25px;text-align:center;background:#080f25;color:#aaa;font-size:13px}
@media(min-width:700px){.feature-list{display:grid;grid-template-columns:repeat(2,1fr)}}
</style>
</head>
<body>

<header>
 <div class="logo"><span>✦</span> JB</div>
 <nav>
  <a href="#accueil">Accueil</a>
  <a href="#services">Services</a>
  <a href="#demo">Démo</a>
 </nav>
</header>

<main>
<section class="hero" id="accueil">
 <div class="tag">✦ POUR LES BOUTIQUES EN LIGNE</div>
 <h1>Votre service client,<br><span>plus intelligent.</span></h1>
 <p>JB aide les boutiques en ligne à répondre aux questions de leurs clients, rapidement et simplement.</p>
 <p>✓ Réponses automatiques<br>
 ✓ Informations sur les produits<br>
 ✓ Assistance multilingue<br>
 ✓ Service disponible 24h/24</p>
 <a class="btn" href="#demo">Essayer la démonstration →</a>

 <div class="card" id="demo">
  <h3>✦ Assistant JB</h3>
  <div id="messages">
   <div class="message">Bonjour ! 👋 Bienvenue chez JB. Comment puis-je vous aider ?</div>
  </div>
  <input id="question" placeholder="Écrivez votre question...">
  <button onclick="sendMessage()">➤</button>
  <p style="color:#777;font-size:11px">Démonstration : réponses simulées.</p>
 </div>
</section>

<section class="features" id="services">
 <h2>Pourquoi choisir JB ?</h2>
 <div class="feature-list">
  <div class="feature">
   <h3>⚡ Réponses rapides</h3>
   <p>Répondez plus rapidement aux questions de vos clients.</p>
  </div>
  <div class="feature">
   <h3>📦 Informations produits</h3>
   <p>Présentez les prix et disponibilités de vos articles.</p>
  </div>
  <div class="feature">
   <h3>🌍 Multilingue</h3>
   <p>Une assistance adaptée à plusieurs langues.</p>
  </div>
  <div class="feature">
   <h3>⏱ Gain de temps</h3>
   <p>Réduisez les réponses répétitives.</p>
  </div>
 </div>
</section>
</main>

<footer>
 <h2>✦ JB</h2>
 Smart Customer Care<br><br>
 © 2026 JB — Prototype de démonstration
</footer>

<script>
function sendMessage(){
 const input=document.getElementById("question");
 const messages=document.getElementById("messages");
 const q=input.value.trim();
 if(!q)return;

 const user=document.createElement("div");
 user.className="message user";
 user.textContent=q;
 messages.appendChild(user);

 const lower=q.toLowerCase();
 let answer="Merci pour votre question ! Cette fonction sera améliorée dans la prochaine version de JB.";

 if(lower.includes("prix")||lower.includes("coût")){
  answer="Les prix sont définis par chaque boutique. Cette démonstration utilise des données fictives.";
 }else if(lower.includes("livraison")||lower.includes("livrer")){
  answer="Les délais de livraison dépendent de la boutique et de votre adresse.";
 }else if(lower.includes("stock")||lower.includes("disponible")){
  answer="La disponibilité dépend du stock réel de la boutique. Cette démo ne consulte pas encore son inventaire.";
 }else if(lower.includes("bonjour")||lower.includes("salut")){
  answer="Bonjour ! 👋 Ravi de vous accueillir. Que souhaitez-vous savoir ?";
 }

 const bot=document.createElement("div");
 bot.className="message";
 bot.textContent=answer;
 messages.appendChild(bot);

 input.value="";
}
</script>
</body>
</html>
