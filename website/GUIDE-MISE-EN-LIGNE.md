# Guide de mise en ligne — elysia.studio

## Ce que tu as

- **Domaine** : elysia.studio (acheté sur Ionos)
- **Site** : un dossier `website/` contenant `index.html`, `favicon.svg`, et `images/`
- **Pas d'hébergement** pour l'instant

---

## Option recommandée : Hébergement IONOS (le plus simple pour toi)

### Étape 1 — Ajouter un hébergement web sur Ionos

1. Connecte-toi sur **https://my.ionos.fr**
2. Va dans **Hébergement** ou **Hosting**
3. Choisis le pack **Essential** (environ 1€/mois la première année) — c'est largement suffisant pour un site vitrine
4. Associe-le à ton domaine **elysia.studio**

### Étape 2 — Accéder au gestionnaire de fichiers

1. Dans ton espace Ionos, va dans **Hébergement > Mon espace web**
2. Clique sur **Gestionnaire de fichiers** (ou WebSpace Explorer)
3. Tu verras un dossier vide (ou avec un fichier index.html par défaut)

### Étape 3 — Uploader les fichiers du site

1. **Supprime** le fichier index.html par défaut s'il existe
2. **Upload** tout le contenu du dossier `website/` :
   - `index.html`
   - `favicon.svg`
   - Le dossier `images/` (avec tous les .jpg dedans)
3. La structure sur le serveur doit être :
   ```
   / (racine)
   ├── index.html
   ├── favicon.svg
   └── images/
       ├── boy-food.jpg
       ├── explorer.jpg
       ├── girl-landscape.jpg
       ├── heroine-horse.jpg
       ├── lion.jpg
       ├── mosque-family.jpg
       └── tea-grandpa.jpg
   ```

### Étape 4 — Activer le SSL (HTTPS)

1. Dans Ionos, va dans **Domaines & SSL**
2. Active le **certificat SSL gratuit** pour elysia.studio
3. Active la redirection HTTP → HTTPS

### Étape 5 — Vérifier

1. Va sur **https://elysia.studio** dans ton navigateur
2. Vérifie que le site s'affiche correctement
3. Teste le switch FR/EN
4. Teste sur mobile (depuis ton téléphone)

---

## Option alternative gratuite : GitHub Pages

Si tu préfères ne rien payer pour l'hébergement :

### Étape 1 — Créer un compte GitHub
1. Va sur **https://github.com** et crée un compte gratuit

### Étape 2 — Créer un dépôt
1. Clique sur **New repository**
2. Nomme-le `elysia-website`
3. Laisse-le en **Public**
4. Clique **Create repository**

### Étape 3 — Uploader les fichiers
1. Clique sur **uploading an existing file**
2. Fais glisser tous les fichiers du dossier `website/` (index.html, favicon.svg, et le dossier images)
3. Clique **Commit changes**

### Étape 4 — Activer GitHub Pages
1. Va dans **Settings > Pages**
2. Source : **Deploy from a branch**
3. Branch : **main**, dossier **/ (root)**
4. Clique **Save**

### Étape 5 — Connecter ton domaine
1. Dans GitHub Pages, ajoute le **Custom domain** : `elysia.studio`
2. GitHub va te demander de configurer les DNS. Va sur Ionos :
   - **DNS > elysia.studio > Ajouter un enregistrement**
   - Type **A** pointant vers les IP GitHub Pages :
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`
   - Type **CNAME** : `www` pointant vers `ton-username.github.io`
3. Attends 10-30 minutes que le DNS se propage
4. Coche **Enforce HTTPS** dans GitHub Pages

---

## Configuration des emails

Pour que les adresses **contact@elysia.studio** et **stories@elysia.studio** fonctionnent :

### Option simple — Redirection email (gratuit sur Ionos)
1. Dans Ionos, va dans **Email > Créer une redirection**
2. Crée `contact@elysia.studio` → redirige vers ton email personnel
3. Crée `stories@elysia.studio` → redirige vers ton email personnel

### Option avancée — Boîte mail Ionos
Ionos propose aussi des boîtes mail payantes si tu veux envoyer depuis @elysia.studio

---

## Pour le compte Apple Developer

Apple demande un **site web fonctionnel** avec :
- Le nom de l'entreprise ✅ (Elysia SAS)
- Une description de l'activité ✅ (story apps for kids)
- Des informations de contact ✅ (email)
- Des mentions légales ✅ (page Legal Notice incluse)

Une fois le site en ligne sur elysia.studio, tu peux utiliser cette URL dans ta demande de compte développeur Apple.

---

## Checklist finale

- [ ] Hébergement activé sur Ionos
- [ ] Fichiers uploadés
- [ ] SSL activé (HTTPS)
- [ ] Site visible sur https://elysia.studio
- [ ] Emails redirigés (contact@ et stories@)
- [ ] Test mobile OK
- [ ] Soumettre l'URL à Apple Developer
