# Ghid de publicare — Site SATOS Medical

Acest folder conține site-ul complet, gata de pus online. Mai jos ai pașii exacți, în ordine.

---

## Ce conține pachetul

**Pagini site (12):**
- `index.html` — Acasă (pagina principală)
- `estetica-faciala.html`
- `cosmetologie.html` — cosmetologie injectabilă
- `epilare-laser.html`
- `remodelare-corporala.html`
- `ultrasonografie.html`
- `masaj.html`
- `fizioterapie.html`
- `laborator.html`
- `confidentialitate.html`, `cookies.html`, `date-medicale.html` — pagini legale

**Fișiere tehnice:**
- `favicon.ico`, `favicon-32.png`, `apple-touch-icon.png` — iconița din tab
- `robots.txt`, `sitemap.xml` — pentru Google (SEO)

Fiecare pagină e un fișier autonom (logo inclus în cod). Nu există fișiere lipsă.

---

## IMPORTANT: înainte de publicare

Site-ul e funcțional, dar are câteva locuri de completat. Le poți pune și după publicare, dar e mai bine înainte:

1. **Email real** — peste tot apare `contact@satos.md` (provizoriu). Caută și înlocuiește în toate fișierele dacă ai altă adresă.
2. **Prețuri** — paginile Masaj au prețuri „___ L" de completat. (Estetică facială și Epilare au prețuri reale.)
3. **Domeniul în sitemap.xml și robots.txt** — acum scrie `satos.md`. Dacă domeniul tău e altul, modifică-l în acele 2 fișiere.
4. **Facebook / Instagram** — încă neadăugate (le punem când ai linkurile).
5. **Revizuire juridică** — paginile legale sunt o bază solidă, dar e recomandat să le verifice un avocat înainte de lansarea oficială.

---

## PASUL 1 — Pune fișierele pe GitHub

Ai deja cont GitHub. Vom crea un depozit (repo) nou și urcăm fișierele.

1. Intră pe github.com, apasă **„+"** (dreapta sus) → **New repository**.
2. Nume repo: `satos-site` (sau cum vrei).
3. Bifează **Public** (sau Private — merge și așa cu Cloudflare).
4. NU bifa „Add README".
5. Apasă **Create repository**.
6. Pe pagina următoare, apasă **„uploading an existing file"** (linkul din mijloc).
7. **Trage toate fișierele** din acest folder în fereastra browserului (toate odată — cele 12 .html + favicon-uri + robots + sitemap).
   - IMPORTANT: urcă **fișierele**, nu folderul. Selectează-le pe toate dinăuntru.
8. Jos, apasă **Commit changes**.

Gata — codul e pe GitHub.

---

## PASUL 2 — Conectează Cloudflare Pages

Ai deja cont Cloudflare. 

1. Intră pe dash.cloudflare.com.
2. În meniul din stânga: **Workers & Pages** → tab **Pages**.
3. Apasă **Connect to Git** (NU „Direct upload").
4. Autorizează accesul la GitHub (dacă cere) și alege repo-ul `satos-site`.
5. La setări de build, lasă TOTUL gol/implicit:
   - **Framework preset:** None
   - **Build command:** (gol)
   - **Build output directory:** `/` (sau lasă implicit)
6. Apasă **Save and Deploy**.

Cloudflare va publica site-ul în ~1 minut. Îți va da o adresă de test, ceva gen `satos-site.pages.dev`. Deschide-o — site-ul e LIVE.

---

## PASUL 3 — Conectează domeniul tău (de la TopHost)

Acum legăm domeniul real.

1. În proiectul tău Pages din Cloudflare → tab **Custom domains** → **Set up a custom domain**.
2. Scrie domeniul tău (ex. `satos.md`) și apasă Continue.
3. Cloudflare îți va arăta niște înregistrări **DNS** (de tip CNAME sau A) pe care trebuie să le adaugi la TopHost.
4. Intră în contul TopHost.MD → secțiunea **DNS / Zone DNS** a domeniului tău.
5. Adaugă înregistrările exact cum ți le dă Cloudflare.
6. Salvează. Propagarea durează de la câteva minute la câteva ore.

După ce DNS-ul se propagă, `satos.md` va arăta site-ul, automat cu **HTTPS** (lacătul verde) și securitate Cloudflare.

---

## PASUL 4 — Cum actualizezi site-ul mai târziu

Foarte simplu, fără cod:
1. Intră pe GitHub → repo-ul `satos-site`.
2. Apasă pe fișierul pe care vrei să-l schimbi (ex. `masaj.html`).
3. Apasă iconița **creion** (Edit).
4. Modifici ce trebuie (preț, text), apoi **Commit changes**.
5. Cloudflare publică automat modificarea în ~1 minut.

Pentru editare și mai ușoară (fără să atingi codul), îți pot adăuga ulterior un mic panou de administrare.

---

## După publicare — recomandări

- **Google Search Console** — adaugă site-ul ca să apară în Google (gratuit).
- **Google Business Profile** — revendică locația SATOS Medical pentru hartă și recenzii.
- **Banner de cookies** — de adăugat (funcție mică).
- **Înregistrare ca operator de date** la CNPDCP — verifică cu un jurist dacă e necesar.

---

Dacă te blochezi la orice pas, spune-mi exact unde ești și ce vezi pe ecran.
