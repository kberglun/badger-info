# badger-info

Publika sidor för Android-appen Badger. Just nu bara integritetspolicyn, som Google Play kräver
en länk till. Appens kod ligger i det privata repot `kberglun/badger`.

Sidan ligger på **https://badger-info.pages.dev/** och publiceras med Cloudflare Pages. Adressen
består bara av projektnamnet, till skillnad från GitHub Pages och Cloudflare Workers, där
kontonamnet ingår i adressen.

## Publicera om efter en ändring

```bash
export PATH=$HOME/.nvm/versions/node/v24.19.0/bin:$PATH
npx wrangler@latest pages deploy . --project-name badger-info --branch main --commit-dirty=true
```

Projektet skapades med `--force`, vilket lade det i klassiska Cloudflare Pages i stället för det
nya Workers-flödet. `--force` behövs bara den gången; senare kommandon hittar projektet av sig
själv.
