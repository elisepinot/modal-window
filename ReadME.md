# modal-window-package

`modal-window-package` est un composant React modulaire et réutilisable conçu pour créer des fenêtres modales élégantes et interactives.

## Lien du package npm

https://www.npmjs.com/package/modal-window-package


## Dépendances

Ce composant est conçu pour être utilisé avec React. Assurez-vous que votre projet utilise React 17.0.0 ou une version ultérieure. Voici les dépendances principales de ce package :

- React (>=18.2.0)
- ReactDOM (>=18.2.0)

Si vous n'avez pas déjà React et ReactDOM dans votre projet, vous pouvez les installer avec la commande suivante :

```bash
npm install react@^18.2.0 react-dom@^18.2.0
```

## Installation

Pour installer ce package, exécutez la commande suivante dans votre terminal :

```bash
npm install modal-window-package
```

## Utilisation
Pour utiliser le composant ModalWindow dans votre projet, suivez les étapes suivantes :

### Etape 1 : Importez le composant ModalWindow

```
import { ModalWindow } from "modal-window-package";
```

### Etape 2: Utilisez le composant dans votre application React



```javascript
function App() {
  const [isOpen, setIsOpen] = React.useState(false);

  return (
    <div>
      <button onClick={() => setIsOpen(true)}>Ouvrir la modale</button>
      <ModalWindow isOpen={isOpen} onClose={() => setIsOpen(false)}>
        <p>Ceci est le contenu de la modale</p>
      </ModalWindow>
    </div>
  );
}
```

Dans cet exemple, isOpen contrôle la visibilité de la modale et onClose est la fonction appelée pour fermer la modale.


### Props
Le composant ModalWindow accepte les props suivantes :

* isOpen : Un booléen qui contrôle la visibilité de la modale.
* onClose : Une fonction appelée lorsque l'utilisateur souhaite fermer la modale.

Dans cet exemple, `isOpen` est un état qui contrôle l'affichage de la modale : quand `isOpen` est `true`, la modale s'affiche ; quand il est `false`, elle est cachée. Le changement d'état est géré par les appels à `setIsOpen`. Le bouton "Ouvrir la modale" modifie cet état en `true`, ce qui ouvre la modale. Lorsque l'utilisateur souhaite fermer la modale, il clique sur le bouton de fermeture qui appelle la fonction `onClose` définie, mettant à jour l'état `isOpen` en `false` pour cacher la modale.

## Personnalisation du style

Des styles par défaut sont appliqués à la fenêtre modale.
Vous pouvez personnaliser le style en surchargeant les classes CSS suivantes :

- `.modal-window-background` : Le fond de ce qui entoure la fenêtre modale (par défaut, un fond semi-transparent vient superposer le reste de la page web)
- `.modal-window` : Le conteneur de la fenêtre modale.
- `.modal-window-close-btn` : Le bouton de fermeture de la fenêtre modale.

Voici un exemple de personnalisation :

```css
.modal-window {
  background: #f0f0f0;
  width: 500px; /* Largeur personnalisée */
}

.modal-window-close-btn {
  background: red; /* Bouton de fermeture personnalisé */
}
```

## Auteur
- [Elise Pinot](https://github.com/elisepinot)

## Licence

Ce projet est sous licence ISC. Cette licence vous permet de :

- **Utiliser** le logiciel à titre gratuit pour usage personnel et commercial.
- **Modifier** le logiciel selon vos besoins.
- **Distribuer** le logiciel à d'autres personnes.
- **Sous-licencier** et **vendre** le logiciel tant que vous incluez la licence originale et les avis de droits d'auteur avec les copies du logiciel.

Cette licence est également permissive dans le sens où elle ne comporte pas de restrictions importantes en termes de responsabilité ou de garantie, ce qui signifie que le logiciel est fourni "tel quel", sans garantie d'aucune sorte.

Pour plus d'informations sur la licence ISC, visitez [ce lien](https://opensource.org/licenses/ISC).
