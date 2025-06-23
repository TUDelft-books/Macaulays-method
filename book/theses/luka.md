# Luka: Variabele stijfheden (in Dutch)

> Macaulay's methode is een variatie op de directe integratie methode om het krachtverloop  
> en de vervorming van een constructie te berekenen. Bij deze methode worden zogeheten  
> singulariteitsfuncties gebruikt om de belasting op constructie met een enkele vergelijking  
> te kunnen beschrijven. Dit heeft als gevolg dat het aantal integratieconstanten laag blijft,  
> wat het oplossen van de constructie minder intensief maakt. Er is echter nog niet beschre-  
> ven hoe deze methode toegepast kan worden op constructies met variërende stijfheden.  
> Gebruikelijk worden delen van de constructie met verschillende stijfheidssituaties apart  
> beschreven. Dit is echter niet in lijn met het idee van Macaulay's methode om de gehele  
> constructie met één vergelijking te beschrijven. Daarom wordt in dit rapport onderzoek  
> gedaan naar de volgende vraag:  
> 
> "Hoe kan de methode van Macaulay toegepast worden op constructies waarbij de stijfheid  
> varieert over de lengte?"  
> 
> Vanuit de definitie van de kromming is gevonden dat een verandering in stijfheid hetzelfde  
> effect heeft als een inverse verandering van het moment. Voor de kromming geldt $ \kappa = \cfrac{M}{EI}$.  
> Een verdubbeling van de stijfheid geeft hetzelfde effect als een halvering van het moment.  
> Hieruit volgt een methode waarbij het effect van belastingen wordt geïntroduceerd in  
> de krommingsvergelijking om het effect van de variërende stijfheid te simuleren. Deze  
> belastingen zijn virtueel genoemd.  
> 
> Een sprong in stijfheid kan gesimuleerd worden met een virtuele puntlast en een virtueel  
> koppel ter plaatse van de sprong. De waarde van deze virtuele belastingen dienen respectievelijk de waarden van de dwarskracht en het moment op dit punt in de constructie te  
> zijn, vermenigvuldigd met de gevonden sprongfactor:  
> 
> $$ nsprong = \left( 1 - \cfrac{EI_1}{EI_2}\right) $$  
> 
> waarbij:  
> 
> - $EI_1$ = buigstijfheid van de balk voor de sprong $\left[\rm{kNm}^2\right]$  
> - $EI_2$ = buigstijfheid van de balk na de sprong $\left[\rm{kNm}^2\right]$  
> 
> Wanneer belastingen zich op een punt bevinden met een hogere x-coördinaat dan de de  
> sprong in stijfheid, dienen ze direct op het moment van optreden gecompenseerd te worden  
> met een virtuele belastingen van dezelfde waarde als deze belasting, vermenigvuldigd met  
> de sprongfactor. In het geval van een q-last na de sprong, moet er ook een virtuele q-last  
> toegepast worden om deze te compenseren.  
> 
> De oplossing van een constructie waarbij de stijfheid een sprong maakt, komt er zo als  
> volgt uit te zien:  
> 
> ```{figure} figures/Figuur_1_Luka.png  
> ---  
> align: center  
> ---  
> Constructie  
> ```  
> 
> ```{figure} figures/Figuur_2_Luka.png  
> ---  
> align: center  
> ---  
> Virtuele situatie  
> ```  
> 
> Waarbij:  
> 
> - $dF_1 = \left(1-\cfrac{EI}{2EI}\right) \cdot A_v$  
> - $dF_2 = \left(1-\cfrac{EI}{2EI}\right) \cdot F$  
> - $dT = \left(1-\cfrac{EI}{2EI}\right) \cdot A_v \cdot \cfrac{L}{2}$  
> 
> Hetzelfde is mogelijk voor constructies met een lineair stijfheidsverloop dat een knik  
> maakt. Hierbij zijn de virtuele belastingen die toegepast dienen te worden een q-last  
> en een puntlast. De waarden hiervan zijn wederom respectievelijk het moment en de  
> dwarskracht op het punt van de knik. Ditmaal worden deze waarden vermenigvuldigd  
> met de knikfactor:  
> 
> $$n_{\rm{knik}} = \cfrac{EI_1 \cdot \left(c_2 - c_1\right)}{\left(EI_1 + c_1 \cdot a + c_2 \cdot \left(x-a\right)\right)\cdot \left(c_1 \cdot x + EI_1 \right)}$$  
> 
> waarbij:  
> 
> - $EI_1$ =  buigstijfheid van de balk op $x=0$ $\left[\rm{kNm}^2\right]$  
> - $c_1$ = helling van stijfheidsverloop voor de knik $\left[\cfrac{\rm{kNm}^2}{\rm{m}}\right]$  
> - $c_1$ = helling van stijfheidsverloop vna de knik $\left[\cfrac{\rm{kNm}^2}{\rm{m}}\right]$  
> - $a$ = x-coördinaat waarop de knik in stijfheid zich bevind $\left[\rm{m}\right]$  
> 
> De oplossing van een constructie waarbij de stijfheid van helling verandert, komt er zo als  
> volgt uit te zien:  
> 
> ```{figure} figures/Figuur_3_Luka.png  
> ---  
> align: center  
> ---  
> Constructie  
> ```  
> 
> ```{figure} figures/Figuur_5_Luka.png  
> ---  
> align: center  
> ---  
> Stijfheidsverloop  
> ```  
> 
> ```{figure} figures/Figuur_4_Luka.png  
> ---  
> align: center  
> ---  
> Virtuele situatie  
> ```  
> 
> Waarbij:  
> 
> - $dF = \cfrac{1}{EI} \cdot \cfrac{1}{x} \cdot \left(A_v + F\right)$  
> - $dq = \cfrac{1}{EI} \cdot \cfrac{1}{x} \cdot \left(A_v + F\right)$  
> 
> Ten slotte is deze methode ook toepasbaar op constructies die belast worden op nor-  
> maalkracht. In dit geval hoeft enkel de normaalkracht virtueel aangepast te worden. In  
> tegenstelling tot het geval voor buiging waar zowel de dwarskracht als het moment aan-  
> gepast worden. Dit geval is dus relatief eenvoudiger dan dat voor buiging. In het geval  
> van een sprong in axiale stijfheid wordt een virtuele puntlast toegepast op het punt van  
> de sprong. In het geval van een knik in lineaire axiale stijfheid is dit een q-last vanaf het  
> punt van de sprong.  

{cite:ts}`luka_2025`

## Documenten
- [Report](./Macaulay's_methode_met_variabele_stijfheden_LKBoersen_5820626.pdf)
- [GitHub repository](https://github.com/lBoersen/Methode-van-Macaulay-met-variabele-stijfheden), examples also shown in this book.