# Opgave: CSS responsive

Gegeven de Cowboy Henk pagina. We zullen deze stap voor stap responsive maken. Aan de HTML hoef je niks te wijzigen. Zet je media queries in responsive.css; je zult echter ook wel wijzigingen moeten doen in styles.css

## Viewport meta

In de `<head>` moet altijd de `<meta name="viewport"...">` staan. Op desktop zul je geen verschil zien, maar op mobiele devices wel: zonder deze regel zal je pagina herschalen (uitzoomen) in plaats van responsive te reageren. 

1. Controleer of deze regel aanwezig is.

## Flexibel maken

Maak het browservenster smaller; je merkt dat de pagina niet flexibel is. De schuldige:

2. op de `body` is `width: 1200px` ingesteld; verander dit naar `max-width`

Controleer of de pagina nu wel flexibel is. 

## Eerste breekpunt: 500px

Een breekpunt is een breedte (in px) vanaf wanneer een genest blok CSS moet uitgevoerd worden. 

3. Voeg een eerste breekpunt toe voor 500px (we werken in `responsive.css`), vanaf wanneer de font-size verandert naar 14px:

```
@media(width >= 500px) {
	body {
		font-size: 14px;
	}
	/* andere stijlen uitgevoerd vanaf 500px */
	/* ... */
}
```

Maak het browservenster smaller/breder, en controleer of vanaf 500px de font-size 14px wordt. In hetzelfde breekpunt, maak nu de volgende transities voor de footer onderaan elke blogpost:

4. verberg in `styles.css` het comments stuk rechtsonder met `display: none`; toon het in `responsive.css` vanaf 500px weer met `display: block`
5. positioneer onder 500px rechts, en boven 500px zover mogelijk uit elkaar (tip: gebruik de `justify-content` flex property)

## Tweede breekpunt: 700px

6. voeg een breekpunt toe voor 700px in `responsive.css`
7. voer in de footer de flex layout pas uit vanaf dit breekpunt
8. aligneer de footer titel links beneden dit breekpunt, en rechts erboven
9. zet een 20px margin onder de footer buttons beneden dit breekpunt, en 0px erboven 

## Derde breekpunt: 900px

10. maak een derde breekpunt op 900px in `responsive.css`
11. zet het hoofdmenu pas horizontaal vanaf dit breekpunt
12. maak twee kolommen in de main pas vanaf dit breekpunt
