# Somatic Recovery — Asistent Virtual

Chatbot AI pentru clinica de fiziokinetoterapie la domiciliu Somatic Recovery (Brașov).

## Ce face
- Răspunde la întrebări despre servicii, prețuri, sfaturi (AI Claude)
- Preia solicitări de programare (nume, telefon, afecțiune, interval orar)
- Trimite automat email la fiecare programare (via EmailJS)

## Tehnologie
- Node.js + Express (backend care ține cheia API secretă)
- HTML/CSS/JS vanilla (frontend)
- Claude API (Anthropic)
- EmailJS (notificări email)

## Variabile de mediu (Railway → Variables)
| Variabilă | Valoare |
|---|---|
| `ANTHROPIC_API_KEY` | Cheia ta de la console.anthropic.com |
| `PORT` | (setat automat de Railway) |

## Rulare locală
```bash
npm install
ANTHROPIC_API_KEY=sk-ant-... npm start
```
Apoi deschide http://localhost:3000

## Deploy pe Railway
1. Urcă acest folder pe GitHub
2. Railway → New Project → Deploy from GitHub repo
3. Adaugă variabila `ANTHROPIC_API_KEY` în tab-ul Variables
4. Railway face build și deploy automat (`npm start`)

## Configurare EmailJS
Cheile EmailJS sunt în `public/index.html` (sunt publice prin design).
Pentru producție, schimbă în template-ul EmailJS adresa "To Email" în
`kineto@somaticrecovery.ro`.
