# Tinus: Springs in SymPy (in Dutch)

> In dit rapport is er onderzocht op welke manier het mogelijk is om verschillende soorten veren toe te voegen aan een al bestaand rekenmodel voor het berekenen van mechanica schema’s van balken.
>
> Het reken model dat wordt gebruikt is een Python bibliotheek genaamd ’SymPy’. In dit model is het mogelijk om vergelijkingen op te lossen die gebruik maken van symbolische wiskunde. Hierdoor is het instaat om mechanica schema’s van balken op te lossen met onbekende reactie krachten. Echter is dit model nog niet compleet, wel is het een open-source programma, wat betekent dat iedereen er met toestemming veranderingen aan kan toevoegen.
>
> De volgende veren zijn geïmplementeerd in het rekenmodel: Verenende oplegging, Veer in een balk en een rotatie veer. Voor deze implementatie is de wet van Hooke gebruikt voor het omschrijven van de veren.
> 
> Voor het mogelijk maken van de implementatie van veren moest het eerst mogelijk zijn om de mogelijkheid te creëren tot het toevoegen van vaste verplaatsingen en rotaties. Dit ging eerst niet door een fout in het huidige model van SymPy die niet correct de Buigstijfheid van een balk toepaste. Na deze oplossing kon de verende oplegging toegevoegd worden. Hierbij was het enige probleem dat het model moeite had met een symbolische randvoorwaarde.
>
> Bij het invoegen van een veer in een balk, liep het programma tegen een ander probleem aan. De implementatie werkt net links van de locatie, terwijl de benodigde dwarskracht net rechts van de locatie werd gebruikt. Dit erkende probleem is vervolgens opgelost.
> 
> Het invoegen van een rotatie veer had vrijwel dezelfde problemen als het invoegen voor de voorgaande twee veren, alleen dan met de rotatie en het moment.
>
> In de nieuwe versie van SymPy, te vinden in deze repository [Sympy 2026](https://github.com/twrijsdijk/sympy). Is het mogelijk gemaakt om veren toe te voegen aan een balk.

{cite:ts}`tinus_2026`

## Documenten
- [GitHub repository](https://github.com/ChrisvanZwol/Macaulay2D) with examples, also shown in this book
- [GitHub repository](https://github.com/twrijsdijk/sympy) with source code.