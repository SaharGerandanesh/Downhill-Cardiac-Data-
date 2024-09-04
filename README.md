# Heart-disease_Project2
              Utforskning av Hjärtdata och Identifiering av Riskfaktorer
1. Introduktion
Presentation av Datasetet:
Vi har analyserat ett dataset som innehåller information om hjärtsjukdomar. Datasetet innehåller 14 variabler inklusive ålder, kön, kolesterolnivåer, blodtryck och målvariabeln target, som indikerar närvaron av hjärtsjukdom (1) eller frånvaro (0).
Syftet med denna analys är att identifiera nyckelvariabler som påverkar risken för hjärtsjukdomar och förstå hur dessa variabler samverkar.
2. Datautforskning
Statistik över Nyckelvariabler:

Ålder: Medelåldern i datasetet är cirka 54 år. Detta antyder att populationen är huvudsakligen medelålders, vilket är en kritisk ålder för hjärtsjukdomar.
Blodtryck: Medelvärdet för vilande blodtryck (trestbps) är cirka 131 mm Hg, vilket är något över normalvärdet, vilket kan indikera hypertoni bland många individer.
Korrelationsmatris: Vi undersökte korrelationerna mellan olika variabler och fann att vissa variabler som maximal hjärtfrekvens (thalach) och ST-depression (oldpeak) har starka korrelationer med målvariabeln.

Observationer:

Positiv korrelation mellan kolesterol och ålder, vilket inte är överraskande då kolesterolnivåer tenderar att öka med åldern.
Negativ korrelation mellan maximal hjärtfrekvens och ålder, vilket visar att äldre personer tenderar att ha lägre maximal hjärtfrekvens.
3. Visualisering
Åldersfördelning:

Histogrammet visar att de flesta patienter är mellan 40 och 65 år gamla, vilket är den åldersgrupp där risken för hjärtsjukdomar är högre.

Blodtryck (trestbps) - Boxplot:

Boxplot visar att det finns flera outliers i blodtrycksdata, vilket kan tyda på patienter med allvarliga blodtrycksproblem.

Scatterplot: Ålder vs. Maximal Hjärtfrekvens:

Detta scatterplot illustrerar en tydlig trend där äldre personer tenderar att ha lägre maximal hjärtfrekvens. De blåa punkterna representerar individer utan hjärtsjukdom, och de röda representerar de med hjärtsjukdom.

4. Datareduktion: Singular Value Decomposition (SVD)
Singular Value Decomposition (SVD):

För att bättre förstå de underliggande mönstren i data använde vi Singular Value Decomposition (SVD). 
Dessa två komponenter förklarar en betydande del av variationen i data, där den första komponenten förklarar cirka 28% av variationen och den andra komponenten förklarar cirka 22%.

Visualisering av SVD-resultat:

SVD-plotten visar tydliga kluster baserat på närvaro av hjärtsjukdom, vilket indikerar att de utvalda variablerna effektivt kan skilja mellan personer med och utan hjärtsjukdom. Denna visualisering stödjer hypotesen att vissa kombinationer av variabler i datasetet är starka indikatorer för hjärtsjukdomar.


5. Sammanfattning och Slutsatser
Viktigaste Insikter:

Ålder och Maximal Hjärtfrekvens är starkt kopplade till hjärtsjukdom. Äldre individer med lägre maximal hjärtfrekvens har en högre sannolikhet att ha hjärtsjukdom.
Blodtryck och Kolesterol är också viktiga variabler att överväga, då höga nivåer av dessa är förknippade med en ökad risk.
PCA har visat att vi kan effektivt reducera komplexiteten i data och ändå bevara en stor del av den underliggande informationen, vilket är användbart för klassificering och diagnos.
Implikationer:

Dessa insikter kan hjälpa läkare att bättre identifiera riskpatienter och tillämpa förebyggande åtgärder tidigare.
Vidare forskning kan inkludera djupare analys av andra variabler, samt att använda dessa insikter i maskininlärningsmodeller för att prediktera hjärtsjukdom.
