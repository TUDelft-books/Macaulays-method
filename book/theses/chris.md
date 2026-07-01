# Chris: Curved beams (in Dutch)

> In dit rapport wordt Macaulay’s methode uitgebreid zodat deze ook toepasbaar is op gekromde constructies. Macaulay’s methode wordt gebruikt om de verplaatsingsfunctie en verlopen van de interne krachten met relatief weinig berekeningen te bepalen. Hierin worden de belastingen op een ligger omschreven in slechts twee functies, $q_z \left(x\right)$ en $q_x \left(x\right)$, waarmee vervolgens de Euler-Bernoulli differentiaalvergelijkingen kunnen worden opgelost. $q_z \left(x\right)$ en $q_x \left(x\right)$ noemen we de belastingvergelijkingen. 
> 
> $$EI \cfrac{d^4 u_z}{dx^4} -q_z \left(x\right) = 0$$
> $$EA \cfrac{d^2 u_x}{dx^2} +q_x \left(x\right) = 0$$
> 
> Het voordeel van deze methode is dat met slechts twee functies de constructie kan worden doorgerekend, in  plaats van de constructie op te delen in segmenten met randvoorwaarden. Hierdoor zijn er tamelijk weinig variabelen om op te lossen. 
> 
> Oorspronkelijk bestond de methode alleen voor rechte ééndimensionale liggers. De laatste jaren hebben  studenten aan de TU Delft de methode verder uitgebreid. Inmiddels is de methode ook toepasbaar op  tweedimensionale geknikte constructies. Naar de toepassing op gekromde constructies was echter nog weinig onderzoek gedaan. Daarom wordt dat in dit rapport gedaan. Zo wordt een breder toepasbare methode voor het doorrekenen van tweedimensionale constructies ontwikkeld.
> 
> De methode die in dit rapport wordt omschreven begint met het beschrijven van de vorm van de constructie met de functies $h\left(x\right)$ en $v\left(x\right)$. Hierin zijn $v$ en $h$ de globale horizontale en verticale richtingen. $x$ en $z$ zijn de lokale axiale en tangentiële richtingen.
> 
> ```{figure} ./figures/figuur_1_chris.jpeg
> :align: center
> Globaal en lokaal assenstelsel
> ```
>
> Met de functies $h \left(x\right)$ en $v \left(x\right)$ kunnen de belastingvergelijkingen worden opgesteld. De formules hiervoor worden in dit rapport afgeleid en staan vermeld in onderstaande vergelijkingen:
> 
> **Koppel**
> 
> $$ q_z \left(x\right) = T \left< x - b \right>^{-2} \quad \text{(3)}$$
> $$ q_x \left(x\right) = 0$$
> 
> **Verticale puntlast**
> 
> $$ q_z \left(x\right) = F_v \left( \left< x - b \right>^{-1} \cfrac{dh}{dx} + \left< x - b \right>^{0} \cfrac{d^2h}{dx^2} \right)$$
> $$ q_x \left(x\right) = F_v \left( \left< x - b \right>^{-1} \cfrac{dv}{dx} + \left< x - b \right>^{0} \cfrac{d^2v}{dx^2} \right)$$
> 
> **Horizontale puntlast**
> 
> $$ q_z \left(x\right) = -F_h \left( \left< x - b \right>^{-1} \cfrac{dv}{dx} + \left< x - b \right>^{0} \cfrac{d^2v}{dx^2} \right)$$
> $$ q_x \left(x\right) = F_h \left( \left< x - b \right>^{-1} \cfrac{dh}{dx} + \left< x - b \right>^{0} \cfrac{d^2h}{dx^2} \right)$$
> 
> **Verticale gelijkmatig verdeelde belasting**
> 
> $$ q_z \left(x\right) = q_v \left( \left< x - b \right>^{0} \cfrac{dh}{dx} + \left< x - b \right>^{1} \cfrac{d^2h}{dx^2} \right)$$
> 
> $$ q_x \left(x\right) = q_v \left( \left< x - b \right>^{0} \cfrac{dv}{dx} + \left< x - b \right>^{1} \cfrac{d^2v}{dx^2} \right)$$
> 
> **Horizontale gelijkmatig verdeelde belasting**
> 
> $$ q_z \left(x\right) = -q_h \left( \left< x - b \right>^{0} \cfrac{dh}{dx} + \left< x - b \right>^{1} \cfrac{d^2h}{dx^2} \right)$$
> 
> $$ q_x \left(x\right) = q_h \left( \left< x - b \right>^{0} \cfrac{dv}{dx} + \left< x - b \right>^{1} \cfrac{d^2v}{dx^2} \right)$$
> 
> Na het viermaal integreren van $q_z\left(x\right)$ en het tweemaal integreren van $q_x\left(x\right)$ worden de verplaatsingen in lokale  assenstelsels gevonden. Om deze om te schrijven tot de verplaatsingen in het globale assenstelsel, zijn onderstaande formules afgeleid.
> 
> $$u_v\left(x\right) = u_{v,z}\left(x\right) + u_{v,x}\left(x\right) = u_x \left(x\right) \cfrac{dv}{dx} + u_z \left(x\right) \cfrac{dh}{dx} - \int_{s=0}^{s=x} \left(u_x\left(s\right) \cfrac{d^2v \left(s\right)}{ds^2} + u_z \left(s\right) \cfrac{d^2h\left(s\right)}{ds^2}\right) ds $$
> 
> $$u_h\left(x\right) = u_{h,z}\left(x\right) + u_{h,x}\left(x\right) = u_x \left(x\right) \cfrac{dh}{dx} + u_z \left(x\right) \cfrac{dv}{dx} - \int_{s=0}^{s=x} \left(u_x\left(s\right) \cfrac{d^2h \left(s\right)}{ds^2} - u_z \left(s\right) \cfrac{d^2v\left(s\right)}{ds^2}\right) ds $$
>
> Hierna kunnen met behulp van randvoorwaarden alle onbekenden worden opgelost. 

{cite:ts}`chris_2026`

## Documenten
- [GitHub repository](https://github.com/ChrisvanZwol/Macaulay2D), also shown in this book