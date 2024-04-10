# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh


Vous allez devoir créer un site de recherche de Pays.

Pour ça, vous allez créer un formulaire de recherche avec un input de type texte et un button envoyer qui vous permettra d'afficher un ou plusieurs pays correspondant à votre recherche.

Si vous tapez "fr" dans la recherche, vous devez afficher la France, mais egalement "Afrique du Sud", "Territoire des Terres australes et antarctiques françaises" etc
Si vous ne tapez rien, alors rien ne s'affiche, car il y a beaucoup trop de pays...

Tous les pays doivent apparaitre en Francais (si possible), avec leur drapeau, leur continent et capitale

1ere etape :
Afficher les pays depuis l'api https://restcountries.com/v3.1/name/fra en stockant le resultat dans un state countries
La definition de ce state est fait dans le .then du fetch

2eme etape : 
Faire un state search, qui est lié a un input de type text
Quand on tape dans l'input, le state est modifié et l'URL d'API également
L'URL d'API ressemblera à : 
https://restcountries.com/v3.1/name/${search}
Lors de la modification du state search, faire en sorte que le useEffect sois relancé afin de remettre a jour la liste des pays 

3eme etape :
Lors du clic sur le pays, une nouvelle page s'ouvre avec en plus :
La liste des devises (nom et symbole)
Les différents langages
Tous les pays frontaliers (Bonus)
et un lien gmap pour retrouver le pays

Ressource :
https://restcountries.com/