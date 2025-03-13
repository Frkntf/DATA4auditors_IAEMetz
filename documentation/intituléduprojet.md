#Ceci est le folder de documentation
[Analyse Apple,Meta,Microsoft_Furkan_Ilies.pdf](https://github.com/user-attachments/files/19230019/Analyse.Apple.Meta.Microsoft_Furkan_Ilies.pdf)


I) Introduction

Dans un marché où la volatilité et la performance sont au cœur des décisions d’investissement, il est essentiel de comprendre comment certaines actions se comportent face à un indice de référence comme le S&P 500. Aujourd’hui, nous allons analyser en détail la rentabilité et le risque des actions Apple, Microsoft et Meta afin de déterminer si elles offrent un meilleur potentiel de rendement ajusté au risque que le marché global.

1)	Présentation du sujet
   
Ce rapport examine en profondeur la performance financière des actions AAPL (Apple Inc.), MSFT (Microsoft Corporation) et META (Meta Platforms Inc.) par rapport au benchmark SPY (SPDR S&P 500 ETF Trust) sur une période de six ans, allant du 12 mars 2019 au 12 mars 2025. Ces entreprises, piliers du secteur technologique, sont analysées à travers des indicateurs financiers clés pour évaluer leur rendement, leur risque et leur comportement par rapport au marché global, représenté par le SPY, un fonds indiciel qui suit l’indice S&P 500.

2)	Objectif de l’étude
   
L’objectif principal est de comparer les performances des actions AAPL, MSFT et META en termes de rendement annualisé, volatilité, beta, alpha et ratio de Sharpe, afin de déterminer leur capacité à générer de la valeur pour les investisseurs par rapport au marché. Cette analyse vise également à identifier les profils risque-rendement distincts de chaque action pour guider les décisions d’investissement.

3)	Contexte et justification
   
AAPL, MSFT et META ont été sélectionnées pour leur domination dans le secteur technologique et leur influence significative sur les indices boursiers mondiaux. Apple est un leader dans les produits électroniques grand public et les services numériques, Microsoft excelle dans les logiciels et le cloud computing, tandis que Meta domine les réseaux sociaux et la réalité virtuelle. Le SPY, qui réplique la performance des 500 plus grandes entreprises américaines, offre une référence robuste pour évaluer la surperformance ou la sous-performance de ces actions technologiques par rapport au marché dans son ensemble.
La période 2019-2025 inclut des événements économiques majeurs tels que la pandémie de COVID-19, des fluctuations des taux d’intérêt ou encore l’essor des technologies numériques, rendant cette analyse particulièrement pertinente pour comprendre la résilience et la croissance de ces entreprises dans un contexte dynamique.

4)	Définitions des indicateurs utilisés

•	Rendement annualisé : Mesure le taux de croissance annuel moyen des rendements, exprimé en pourcentage. Il reflète la performance globale de l’investissement sur la période.
•	Volatilité annualisée : Indicateur de risque calculé comme l’écart-type des rendements journaliers, annualisé. Une volatilité élevée signale une plus grande incertitude.
•	Beta : Mesure la sensibilité d’une action aux mouvements du marché (SPY). Un beta > 1 indique une volatilité supérieure au marché, un beta < 1 une moindre volatilité.
•	Alpha : Représente la surperformance ou la sous-performance d’une action par rapport au rendement attendu selon son beta, ajustée pour le risque systématique.
•	Ratio de Sharpe : Évalue le rendement excédentaire au-dessus du taux sans risque par unité de risque. Un ratio plus élevé indique un meilleur compromis entre le risque et le rendement.
Ces indicateurs forment ainsi une base solide pour une analyse quantitative et qualitative des performances.

II) Méthodologie

1)	Collecte des données
   
Les données historiques des prix de clôture ajustés ont été extraites via la bibliothèque Python yfinance, une source fiable pour les données financières. Les bibliothèques Python numpy, pandas, matplotlib, seaborn ont été utilisées pour le traitement des données. Les tickers analysés sont AAPL, MSFT, META et SPY, sur la période du 12 mars 2019 au 12 mars 2025.

2)	Traitement des données
   
Les rendements journaliers ont été calculés selon la formule suivante :
Rendement journalier = (Prix de clôture t / Prix de clôture t-1) - 1
Les séries temporelles ont été alignées pour garantir que les dates correspondent entre les actions et le benchmark, éliminant les données manquantes ou aberrantes.

3)	Calcul des indicateurs
   
Les indicateurs ont été calculés de cette manière :
•	Rendement annualisé : Moyenne des rendements journaliers × 252 (jours de trading par an).
•	Volatilité annualisée : Écart-type des rendements journaliers × √252.
•	Beta : Coefficient de régression linéaire des rendements journaliers de l’action sur ceux du SPY, obtenu via une régression simple.
•	Alpha annualisé : Intercept de la régression linéaire, multiplié par 252 pour refléter une valeur annuelle.
•	Ratio de Sharpe : (Rendement annualisé - Taux sans risque) / Volatilité annualisée, avec un taux sans risque fixé à 2%.

4)	Graphiques
   
Cinq graphiques ont été produits pour enrichir l’analyse :
1.	Scatter plot : Positionne chaque action selon son rendement et sa volatilité annualisés.
2.	Rendements cumulés : Courbes montrant l’évolution des rendements cumulés sur la période.
3.	Histogrammes : Distribution des rendements journaliers pour chaque action.
4.	Évolution du ratio de Sharpe : Calculé sur une fenêtre glissante de 252 jours (1 an).
5.	Heatmap : Matrice des corrélations entre les indicateurs (rendement, volatilité, beta, alpha, ratio de Sharpe).
Ces graphiques permettent une interprétation visuelle et intuitive des données.

III) Résultats
1)	Tableau de performance

Le tableau ci-dessous présente les indicateurs calculés pour chaque action :
Action	Rendement annualisé	Volatilité annualisée	Beta	Alpha annualisé	Ratio de Sharpe
AAPL	31.92%	30.66%	1.20	13.87%	0.98
MSFT	25.38%	29.08%	1.19	7.44%	0.80
META	30.21%	42.38%	1.32	10.36%	0.67
Ces chiffres offrent une vue d’ensemble des performances et des risques associés à chaque action.

2)	Analyse des graphiques

a)	Scatter plot (Rendement vs Volatilité)

Le scatter plot positionne les actions dans un espace bidimensionnel où le rendement est représenté en ordonnée et la volatilité en abscisse. AAPL, avec un rendement de 31,92% et une volatilité de 30,66%, se situe dans une zone de rendement élevé et de volatilité modérée, indiquant une capacité à générer des gains importants tout en maintenant une exposition raisonnable au risque. MSFT, avec un rendement de 25,38% et une volatilité de 29,08%, présente un rendement légèrement inférieur à celui d’AAPL, mais sa volatilité plus faible en fait une option relativement stable. Enfin, META, qui affiche un rendement de 30,21% mais une volatilité de 42,38%, offre un rendement similaire à AAPL, mais avec une volatilité beaucoup plus élevée, la positionnant ainsi dans une zone de risque accru.
AAPL domine grâce à son positionnement optimal, combinant un rendement élevé avec une volatilité contenue. MSFT suit de près, offrant une alternative moins volatile mais avec un rendement moindre. META, malgré un rendement compétitif, est pénalisée par une volatilité excessive, suggérant des fluctuations importantes qui pourraient effrayer les investisseurs prudents. Comparé au SPY (rendement typiquement plus faible, autour de 10-12% avec une volatilité moindre), ces actions technologiques affichent une prime de risque significative.

b)	Rendements cumulés

Les courbes des rendements cumulés illustrent l’évolution des investissements au cours de la période étudiée. 
AAPL enregistre un rendement cumulé d'environ 400%, avec une trajectoire exponentielle, marquée par une forte croissance après 2020. MSFT, avec un rendement cumulé d'environ 350%, suit une progression plus linéaire, ce qui reflète la stabilité de son modèle économique centré sur le cloud et les logiciels d'entreprise. META, quant à elle, atteint environ 300%, avec des phases de forte croissance, comme en 2021 lors du boom des revenus publicitaires, mais aussi des corrections importantes, notamment en 2022 à cause des incertitudes liées au métavers. Enfin, SPY, en comparaison, enregistre un rendement cumulé d'environ 150%, suivant une trajectoire plus modeste, caractéristique d'un indice diversifié.
La surperformance des trois actions par rapport au SPY est évidente, avec AAPL en tête grâce à une croissance constante et robuste. MSFT montre une résilience impressionnante, tandis que META, bien que performante, subit des variations plus marquées, probablement liées à des défis stratégiques (ex. : pivot vers le métavers, concurrence dans la publicité). Ces courbes soulignent l’attractivité des valeurs technologiques dans un marché haussier, mais aussi la nécessité de tolérer des fluctuations pour META.

c)	Histogrammes des rendements journaliers
 
Les histogrammes illustrent la distribution des rendements journaliers des actions étudiées. Pour AAPL, la distribution est quasi-normale, centrée autour de 0, avec des rendements variant de -10% à +10%. Les queues de la distribution sont modérées, ce qui reflète une volatilité gérable. MSFT présente une distribution similaire, mais légèrement plus étroite, avec des rendements allant de -15% à +15%, et moins d'événements extrêmes qu'AAPL, ce qui confirme sa stabilité relative. En revanche, META affiche une distribution plus large, s'étendant de -20% à +20%, avec des queues épaisses, ce qui indique des mouvements journaliers plus fréquents et plus prononcés.
META se distingue par une dispersion plus importante, ce qui corrobore sa volatilité élevée (42.38%). Par exemple, des baisses ou hausses quotidiennes de 10% ou plus sont plus fréquentes pour META que pour AAPL ou MSFT, reflétant des réactions exacerbées aux nouvelles (ex. : scandales, résultats trimestriels). AAPL et MSFT, avec des distributions plus resserrées, offrent une prévisibilité supérieure, ce qui est rassurant pour les investisseurs à long terme.

d)	Évolution du ratio de Sharpe

L’évolution du ratio de Sharpe sur une fenêtre glissante de 252 jours met en évidence les variations du rendement ajusté au risque pour chaque action. AAPL présente un ratio stable, oscillant entre 0 et 0,20, avec des pics notables en 2020-2021, lors de la forte croissance post-COVID, et une légère baisse en 2022, en raison du marché baissier. MSFT suit une trajectoire similaire, mais son ratio est légèrement plus bas, oscillant entre 0 et 0,15, avec moins de volatilité, ce qui reflète une performance plus constante. En revanche, META affiche un ratio de Sharpe plus erratique, atteignant 0,20 en 2021, une année particulièrement favorable pour la publicité, avant de chuter à -0,10 en 2022, en raison des difficultés liées au métavers et à la concurrence.
AAPL et MSFT maintiennent un ratio de Sharpe positif et relativement stable, ce qui indique une capacité à générer des rendements ajustés au risque constants, même dans des périodes de turbulence. META, en revanche, montre une forte variabilité, avec des périodes de surperformance spectaculaire suivies de phases de sous-performance. Cela reflète un profil plus spéculatif, où le timing de l’investissement joue un rôle crucial.

e)	Heatmap des corrélations 

Le rendement et l'alpha présentent logiquement une corrélation très forte de 0,95 car l'alpha mesure la surperformance associée au rendement excédentaire. En revanche, la corrélation entre le ratio de Sharpe et la volatilité est négative (-0,77), ce qui indique qu'une volatilité plus élevée tend à réduire le rendement ajusté au risque. De plus, la corrélation entre le ratio de Sharpe et le beta est également négative (-0,81), suggérant que les actions ayant un beta élevé, donc plus sensibles au marché, ont tendance à afficher un ratio de Sharpe plus faible. Enfin, la corrélation entre la volatilité et le beta est positive (0,65), ce qui confirme que les actions présentant une forte volatilité sont généralement plus corrélées au marché.

3)	Analyse des métriques
   
•	Ratio de Sharpe : 
Le ratio de Sharpe de AAPL est de 0,98, proche de 1, ce qui est généralement considéré comme excellent. Cela indique que chaque unité de risque prise par l'investisseur est presque entièrement compensée par du rendement. En revanche, MSFT présente un ratio de Sharpe de 0,80, qui est solide mais légèrement inférieur à celui d’AAPL, suggérant une performance légèrement moins optimisée par unité de risque. Enfin, le ratio de Sharpe de META est de 0,67, plus faible, ce qui reflète un rendement élevé mais dilué par une volatilité excessive.
•	Beta : 
META a le coefficient le plus élevé avec un beta de 1,32. Cela signifie que l'action est particulièrement sensible aux mouvements du marché, amplifiant ainsi les gains en période haussière mais également les pertes en période baissière. AAPL et MSFT présentent des betas similaires, respectivement de 1,20 et 1,19. Ces valeurs montrent qu'elles suivent également le marché avec une volatilité légèrement supérieure, mais restent relativement gérables en comparaison à META.
•	Alpha : 
AAPL se distingue avec un alpha de 13,87 %, indiquant une surperformance exceptionnelle. Cette surperformance est probablement attribuée à des facteurs spécifiques à l'entreprise, comme son innovation continue et la fidélité de ses clients. META présente un alpha de 10,36 %, ce qui reste notable, mais inférieur à celui d'AAPL. Cet alpha est probablement dû à des succès publicitaires, bien qu'il soit tempéré par des incertitudes stratégiques, notamment liées à ses investissements dans le métavers. MSFT, enfin, affiche un alpha de 7,44 %, positif mais plus modeste, ce qui reflète une croissance stable, mais moins dynamique comparée à AAPL et META.
Ainsi, AAPL se présente comme un choix optimal pour un équilibre entre rendement et risque, particulièrement adapté à ceux recherchant une performance robuste avec une volatilité maîtrisée. MSFT, quant à elle, est idéale pour les investisseurs privilégiant la stabilité et une croissance prévisible, tout en offrant un risque modéré. Enfin, META convient davantage aux investisseurs tolérants au risque, prêts à accepter des fluctuations importantes pour bénéficier d’un potentiel de rendement élevé.

IV) Conclusion

L’analyse des performances financières des actions AAPL, MSFT et META sur la période 2019-2025 met en lumière des profils distincts.
•	AAPL se distingue avec un rendement annualisé de 31,92 %, une volatilité modérée de 30,66 %, un ratio de Sharpe de 0,98 et un alpha de 13,87 %. Elle offre ainsi le meilleur équilibre entre risque et rendement, avec une surperformance exceptionnelle par rapport au SPY.
•	MSFT, quant à elle, affiche un rendement de 25,38 %, une volatilité de 29,08 %, un ratio de Sharpe de 0,80 et un alpha de 7,44 %. Cette action représente une option stable et fiable, idéale pour les investisseurs plus prudents.
•	META atteint un rendement de 30,21 %, mais sa volatilité élevée de 42,38 % et son ratio de Sharpe plus faible de 0,67 la rendent plus risquée, bien qu’elle présente un alpha solide de 10,36 %.
Ainsi, en termes de recommandations pour les investisseurs :
•	AAPL est recommandée pour ceux qui recherchent une combinaison optimale de rendement élevé et de risque maîtrisé.
•	MSFT est préférable pour les investisseurs averses au risque, cherchant une stabilité et une croissance régulière.
•	META, quant à elle, est plus adaptée aux investisseurs agressifs, prêts à tolérer des fluctuations importantes pour un potentiel de gains élevé.
Toutes les actions surpassent le SPY, ce qui confirme l’attractivité du secteur technologique. Toutefois, le choix dépendra du profil de risque et des objectifs spécifiques de chaque investisseur.

Cette analyse soulève une question plus large : dans un environnement financier en constante évolution, comment les investisseurs peuvent-ils optimiser leurs décisions pour allier performance et maîtrise du risque ? L’intégration de nouvelles approches, comme l’analyse quantitative avancée ou l’intelligence artificielle, pourrait être une piste pour affiner encore davantage l’évaluation des opportunités d’investissement.
