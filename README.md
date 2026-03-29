<h1># TIPE-Solar-tracker-</h1>

<p>
  <strong>Auteur :</strong> AL BYDEOI Othmen<br>
  <strong>Numéro de candidat concours SCEI :</strong> 12807<br>
  <strong>Thème du tipe :</strong> Transition, Conversion, Transformation
</p>

<hr>

<h2>📝 Introduction et Motivation</h2>
<p>
  Lors de ma dernière année de lycée, j’ai participé à un projet passionnant visant à installer des panneaux solaires sur le toit d’une station de recharge électrique. Afin d’optimiser leur efficacité, nous avons pris la décision risquée mais prometteuse d'ajouter des suiveurs solaires. C'était là ma première rencontre avec cette technologie. J'ai donc décidé de l’étudier.
</p>
<p>
  Quelles interactions le rayonnement solaire entretient-il avec les suiveurs pour assurer leur bon fonctionnement ? Le dispositif doit-il être bien structuré pour améliorer son rendement énergétique au fil des saisons ? Si le suiveur solaire aide à orienter précisément les panneaux tout au long de la journée, cela augmente considérablement l'énergie produite. Le rendement dépendra donc de l'angle de position des panneaux solaires. Mon objectif est de trouver un bon rendement énergétique.
</p>

<hr>

<h2>⚙️ Détails du Prototype</h2>
<p>Le système repose sur une structure mobile motorisée pilotée par intelligence embarquée :</p>
<ul>
  <li><strong>Microcontrôleur :</strong> Carte Arduino Uno.</li>
  <li><strong>Actionneur :</strong> Servomoteur MG995 (pour la rotation).</li>
  <li><strong>Capteurs :</strong> Deux photo-résistances (LDR) montées en différentiel.</li>
  <li><strong>Structure :</strong> Châssis avec panneau incliné à 45°.</li>
</ul>

<hr>

<h2>💻 Fonctionnement du Système</h2>
<p>
  Le programme compare en permanence l'intensité lumineuse reçue par les deux capteurs LDR. Si un déséquilibre est détecté (le soleil a bougé), l'Arduino commande au servomoteur d'ajuster l'angle du panneau pour revenir face à la source de lumière maximale.
</p>

<pre><code>
// Logique simplifiée du code
int difference = valeurGauche - valeurDroite;

if (difference > seuil) {
    monServo.write(angle++); // Tourne vers la lumière
} else if (difference < -seuil) {
    monServo.write(angle--); // Tourne vers la lumière
}
</code></pre>

<hr>

<h2>📚 Bibliographie et Analyse</h2>
<p>
  Un tracker solaire est un dispositif visant à améliorer l’orientation des panneaux photovoltaïques en suivant le mouvement du soleil au long de la journée. Deux technologies majeures sont utilisées : le suivi sur un axe et le suivi sur deux axes. Les systèmes à un axe sont positionnés horizontalement dans un mouvement d’est en ouest, tandis que les deux axes ajoutent également une inclinaison verticale, ce qui permet un suivi plus précis selon les saisons.
</p>
<p>
  L’installation de suiveurs solaires permet d’augmenter la production d’électricité photovoltaïque de <strong>25 à 50 %</strong> par rapport à un système fixe. Bien que cette technologie présente une complexité technique et un coût supérieur, elle est particulièrement adaptée aux grandes installations où le surcoût est compensé par la rentabilité à long terme.
</p>
<p>
  <strong>Conclusion :</strong> Malgré les défis techniques et économiques, les suiveurs solaires ont une forte influence sur l’efficacité de la production d’énergie renouvelable à grande échelle.
</p>
