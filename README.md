# Cave à bière — PWA iPhone et iPad

## Fichiers
Tous les fichiers de ce dossier doivent être publiés ensemble à la racine du site GitHub Pages (ou dans le même sous-dossier). Ne pas ouvrir directement `index.html` depuis Finder : les Service Workers exigent HTTPS (ou localhost).

## Mise en ligne depuis Phenix Code
1. Ouvrir le dossier dans Phenix Code.
2. Placer les 7 fichiers sur un dépôt GitHub Pages (le dépôt doit être public si vous utilisez GitHub Pages gratuit).
3. Dans GitHub > Settings > Pages, publier la branche contenant les fichiers.
4. Ouvrir l'adresse HTTPS du site sur Safari iPhone ou iPad **avec Internet**.
5. Attendre que la page soit chargée, puis Partager > Sur l'écran d'accueil > Ajouter.
6. Ouvrir l'icône créée et tester en mode avion (sans Internet).

## Sécurité et limites
- Aucune API QR externe : génération 100 % locale, sans envoi des données bancaires à un tiers par le code de l'application.
- Le code HTML, JavaScript et les coordonnées bancaires restent **publics** sur GitHub Pages public. Ce n'est PAS une protection par mot de passe. Ne pas y placer de secret.
- Première visite, installation, mises à jour : connexion Internet nécessaire.
- Le cache peut être effacé par iOS, ce qui obligera à recharger le site avec Internet.
- Les paiements ne sont pas encaissés ou vérifiés par l'application : elle ne fait que produire un QR EPC/SEPA.
- Vérifier sur une application bancaire que le QR EPC est reconnu et que bénéficiaire, IBAN, montant et communication sont corrects avant utilisation réelle. Certaines banques ne prennent pas en charge les QR EPC.
- La bibliothèque QR locale dérive de QRCode for JavaScript de Kazuhiko Arase, licence MIT (voir LICENSE-QR.txt).

## Paramètres
Changer BENEFICIARY, IBAN, BIC et COMMUNICATION dans app.js si nécessaire. Après mise à jour, modifier la version du cache dans sw.js pour forcer une mise à jour du cache.
