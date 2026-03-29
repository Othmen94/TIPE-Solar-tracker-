<h1>TIPE-Solar-tracker- </h1>

<p>
  <strong>Auteur :</strong> AL BYDEOI Othmen <br>
  <strong>N°Candidat SCEI:</strong> n°12807 <br>
  <strong>Thème du tipe:</strong> Transition, Conversion, Transformation 
</p>

<hr>

<h2>📝 Présentation du projet</h2>
<p>
  Lors de ma dernière année de lycée, j’ai participé à un projet passionnant visant à installer des panneaux solaires sur le toit d’une station de recharge électrique. Afin d’optimiser leur efficacité, nous avons pris la décision risquée mais prometteuse d'ajouter des suiveurs solaires. C'était là ma première rencontre avec cette technologie. J'ai donc décidé de l’étudier.
</p>

<h3>Problématique</h3>
<p>
  <em>"Le système de suivi solaire permet-il d'améliorer la performance énergétique par rapport à un panneau solaire ?"</em> [cite: 2]
</p>
<p>
  Quelles interactions le rayonnement solaire entretient-il avec les suiveurs pour assurer leur bon fonctionnement ? Le dispositif doit-il être bien structuré pour améliorer son rendement énergétique au fil des saisons ? Mon objectif est de trouver un bon rendement énergétique.
</p>

<hr>

<h2>⚙️ Modélisation et Prototypage </h2>
<p>Le prototype repose sur une structure orientée à <strong>45°</strong> [cite: 60] et utilise les composants suivants :</p>
<ul>
  <li><strong>Microcontrôleur :</strong> Carte Arduino Uno.</li>
  <li><strong>Actionneur :</strong> Servomoteur MG995[cite: 81].</li>
  <li><strong>Capteurs :</strong> Capteurs de lumière (LDR)[cite: 84].</li>
  <li><strong>Composants secondaires :</strong> Résistance, pont en H et fils électriques[cite: 72, 83, 85].</li>
</ul>

<hr>

<h2>💻 Programmation et Fonctionnement [cite: 23]</h2>
<p>
  Le code Arduino compare l'intensité lumineuse entre deux LDR. Si une différence est détectée, le servomoteur ajuste la position du panneau[cite: 107].
</p>

<pre><code>
// Extrait du code source [cite: 96, 106, 108]
int difference = valueLeft - valueRight;

if (difference > 0) {
    currentAngle += 1; // Déplace légèrement à gauche
} else if (difference < 0) {
    currentAngle -= 1; // Déplace légèrement à droite
}
</code></pre>

<hr>

<h2>📚 Bibliographie et Analyse</h2>
<p>
  Un tracker solaire est un dispositif visant à améliorer l’orientation des panneaux photovoltaïques en suivant le mouvement du soleil au long de la journée. 
</p>
<ul>
  <li><strong>Technologies :</strong> Suivi sur un axe (horizontal) ou deux axes (horizontal et vertical).</li>
  <li><strong>Avantages :</strong> Augmentation de la production d'électricité de <strong>25 à 50 %</strong> par rapport à un système fixe.</li>
  <li><strong>Limites :</strong> Complexité technique et coût plus élevé.</li>
</ul>
<p>
  <strong>Conclusion :</strong> Bien que les suiveurs solaires imposent des difficultés techniques et économiques, ils ont une forte influence sur la production d’énergie, notamment dans des installations commerciales ou industrielles à grande échelle. [cite: 114]
</p>
