# TDevTools

**Une boîte à outils gratuite pour les développeurs : 47 outils pour JSON, XML, schémas, API, encodage et certificats, sur macOS, Windows et Linux.**

Par [transposal.app](https://transposal.app)

**Lire dans une autre langue :** [English](README.md) · [Español](README.es.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Türkçe](README.tr.md) · [日本語](README.ja.md) · [简体中文](README.zh-CN.md) · [हिन्दी](README.hi.md)

> **🔒 Fonctionne localement. Vos données ne quittent jamais votre ordinateur.** TDevTools traite tout sur votre machine. Vos fichiers JSON et XML, jetons, clés et certificats ne sont ni téléversés ni envoyés à des services d'analyse. Aucun compte ni suivi. L'application ne se connecte à Internet que si vous le demandez : chargement d'une URL, requête de test vers votre API ou consultation du certificat d'un serveur. Tous les autres outils fonctionnent hors ligne.

## Captures d'écran

**JSON → JSON Schema :** déduisez un schéma à partir de données d'exemple.

![JSON vers JSON Schema](screenshots/json-to-schema.png)

**Testeur d'API :** envoyez des requêtes et consultez les réponses en arborescence, tableau ou texte.

![Testeur d'API](screenshots/api-tester.png)

**Inspecteur de certificats :** examinez la chaîne de certificats et vérifiez les certificats et signatures.

![Inspecteur de certificats](screenshots/certificate-inspector.png)

## Téléchargement

Téléchargez la dernière version sur la page des [versions](https://github.com/siddiquin/TDevTools-releases/releases/latest).

| Système | Fichier |
| --- | --- |
| macOS, Apple Silicon (M1–M4) | `TDevTools-<version>-arm64.dmg` |
| macOS, Intel | `TDevTools-<version>-x64.dmg` |
| Windows 10/11, 64 bits | `TDevTools-Setup-<version>-x64.exe` |
| Windows 10/11, ARM | `TDevTools-Setup-<version>-arm64.exe` |
| Windows, portable | `TDevTools-Portable-<version>.exe` |
| Linux, 64 bits (x86_64) | `TDevTools-<version>-x86_64.AppImage` |
| Linux, ARM64 | `TDevTools-<version>-arm64.AppImage` |

**Configuration requise :** macOS 12 Monterey ou ultérieur ; Windows 10 ou 11 (64 bits ou ARM64) ; ou une distribution Linux récente 64 bits (Ubuntu 20.04+, Debian 11+, Fedora 36+ ou équivalent). Environ 300 Mo d'espace disque.

## Installation

### macOS

1. Téléchargez le fichier `.dmg` adapté, ouvrez-le et acceptez le contrat de licence.
2. Faites glisser **TDevTools** dans **Applications**, puis éjectez l'image disque.
3. Au premier lancement, macOS peut indiquer que l'application ne peut pas être vérifiée, car elle n'est pas signée avec un certificat Apple Developer payant. C'est normal ; l'autorisation n'est nécessaire qu'une fois.
   - **macOS 14 ou antérieur :** dans le Finder, faites un clic droit sur TDevTools, choisissez **Ouvrir**, puis confirmez.
   - **macOS 15 ou ultérieur :** essayez de lancer l'application et cliquez sur **Terminé** dans l'alerte. Ouvrez **Réglages Système → Confidentialité et sécurité**, puis cliquez sur **Ouvrir quand même** à côté du blocage de TDevTools. Confirmez.
4. Si macOS indique que « TDevTools est endommagé », vérifiez d'abord le téléchargement depuis la page officielle des [versions](https://github.com/siddiquin/TDevTools-releases/releases/latest). Dans Terminal, exécutez ensuite `xattr -dr com.apple.quarantine /Applications/TDevTools.app` pour retirer le marqueur de téléchargement de cette application.

### Windows

- **Installateur :** lancez `TDevTools-Setup-<version>-x64.exe` (ou le fichier `arm64` pour un PC ARM), acceptez le contrat et cliquez sur **Installer**. Si SmartScreen affiche « Windows a protégé votre ordinateur », choisissez **Informations complémentaires → Exécuter quand même**. L'installation est limitée à votre compte et ne requiert pas de droits administrateur.
- **Version portable :** lancez `TDevTools-Portable-<version>.exe`. Si SmartScreen intervient, choisissez **Informations complémentaires → Exécuter quand même**.

### Linux (AppImage)

Téléchargez le fichier adapté, autorisez son exécution via **Propriétés → Permissions** ou `chmod +x TDevTools-*.AppImage`, puis ouvrez-le ou lancez-le depuis un terminal. Si le démarrage échoue, certaines distributions nécessitent FUSE 2 (Ubuntu/Debian : `sudo apt install libfuse2` ; Ubuntu 24.04 : `sudo apt install libfuse2t64` ; Fedora : `sudo dnf install fuse-libs`). Gear Lever ou AppImageLauncher peut ajouter l'application au menu.

## Mise à jour et désinstallation

Téléchargez la nouvelle version et installez-la de la même façon ; vos préférences sont conservées. Sur macOS, remplacez l'application dans Applications ; sous Windows, lancez le nouvel installateur ; sous Linux, remplacez l'AppImage.

- **macOS :** placez TDevTools dans la Corbeille. Pour supprimer aussi les préférences, effacez `~/Library/Application Support/TDevTools`.
- **Windows :** désinstallez TDevTools dans **Paramètres → Applications → Applications installées**. Pour supprimer les préférences, effacez `%APPDATA%\TDevTools`. Pour la version portable, supprimez le `.exe`.
- **Linux :** supprimez l'AppImage. Pour supprimer les préférences, effacez `~/.config/TDevTools`.

L'application ne conserve que vos préférences (thème, langue, etc.), jamais de copie de vos données, mots de passe ou clés.

## Fonctionnalités

- **Formater et valider :** formateur, validateur, réparation et édition visuelle JSON ; conversions JSON, XML, CSV, Excel, YAML, TOON et JSONL ; Markdown et schémas JSON/XML (XSD) ; génération de types TypeScript.
- **Sécurité :** décodage, vérification et signature JWT ; encodage Base64/URL/SAML ; empreintes MD5, SHA-1 et SHA-256 ; génération de certificats autosignés et kits mTLS ; inspection de certificats, clés publiques et magasins JKS.
- **Affichage et API :** JSON en arborescence, tableau, grille, graphe et texte ; navigateur OpenAPI/Swagger, client HTTP OAuth2 et mTLS, lecteur SOAP/WSDL, lecteur de fichiers et aperçu Markdown.
- **Requêtes et transformations :** testeur JSONPath, recherche/remplacement par expressions régulières, mappage JSON exportable en JavaScript, TypeScript, Python ou C# ; Transposal Mapper, service cloud premium facultatif.
- **Comparaison :** différences structurelles JSON/XML et validation de schémas JSON avec erreurs par ligne.
- **Dans toute l'application :** 8 langues, 6 thèmes, couleurs d'accent, densité et zoom, copie en un clic, menu contextuel, glisser-déposer et utilisation CPU/mémoire dans la barre d'état.

## Confidentialité et sécurité

- Tous les traitements se font sur votre ordinateur ; rien de ce que vous collez ou ouvrez n'est téléversé.
- Aucun compte, télémétrie ni publicité.
- Connexion réseau uniquement à votre demande, par exemple pour charger une URL, tester une API ou récupérer un certificat.
- Mots de passe, jetons et clés privées conservés en mémoire uniquement pendant l'exécution ; seules vos préférences sont enregistrées.
- Fenêtres isolées et politique de sécurité stricte ; les aperçus HTML n'exécutent pas de scripts ; confirmation avant l'ouverture d'un programme ou script ; les identifiants ne sont envoyés qu'au serveur choisi.
- Les exemples intégrés utilisent des serveurs de démonstration publics, limités à une requête toutes les 2 minutes. Aucune limite pour vos propres URL et fichiers.

## Questions fréquentes

**TDevTools est-il gratuit ?** Oui, il est gratuit pour les développeurs. Consultez le [contrat de licence](LICENSE.md).

**Fonctionne-t-il hors ligne ?** Oui, sauf pour les fonctions qui communiquent avec un serveur choisi par vos soins (chargement d'URL, tests API/SOAP, récupération d'une chaîne de certificats).

**Le code source est-il disponible ?** TDevTools est un logiciel propriétaire. Vous pouvez demander le code par e-mail à **<support@transposal.app>**, avec l'objet « TDevTools ».

**Pourquoi mon ordinateur affiche-t-il un avertissement ?** L'application n'est pas signée avec un certificat développeur Apple ou Microsoft payant. Gatekeeper et SmartScreen affichent donc un avertissement au premier lancement. Suivez les étapes d'installation et téléchargez uniquement depuis la page officielle des [versions](https://github.com/siddiquin/TDevTools-releases/releases/latest).

## Licence et assistance

- [Contrat de licence utilisateur final](LICENSE.md) : utilisation gratuite, sans garantie. Le contrat complet est disponible en 8 langues dans l'application, sous **Aide → Contrat de licence**.
- [Avis sur les logiciels tiers](THIRD_PARTY_NOTICES.md)
- Assistance : **<support@transposal.app>**
- Site web : [transposal.app](https://transposal.app)

© 2026 Transposal. Tous droits réservés.