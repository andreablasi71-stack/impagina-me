# impagina.me

Sito e laboratorio editoriale di **Andrea Blasi** — grafica editoriale, automazioni di produzione e intelligenza artificiale locale.

Online su <https://impagina.me> · pubblicato con GitHub Pages.

---

## Cosa c'è dentro

| File | A cosa serve |
|------|--------------|
| `index.html` | La homepage. Presentazione de "Il laboratorio editoriale", come è fatto e cosa offre |
| `laboratorio-editoriale.md` | Il testo integrale dello stack e dei servizi offerti dal laboratorio |
| `404.html` | Pagina mostrata quando un indirizzo non esiste |
| `robots.txt` | Istruzioni per i motori di ricerca |
| `sitemap.xml` | L'elenco delle pagine per i motori di ricerca |
| `CNAME` | Il dominio personalizzato. **Lo crea GitHub da solo**, non va scritto a mano |

Nessuna dipendenza esterna: niente font da scaricare, niente librerie, niente tracciamento.
La pagina è veloce, leggera e si adatta da sola al tema chiaro o scuro del visitatore.

## Come si modifica il testo

Si apre `index.html` e si scrive dentro.
Salvato il file, si pubblica così:

```bash
git add index.html laboratorio-editoriale.md
git commit -m "docs: aggiorna contenuti laboratorio editoriale"
git push
```

GitHub rimette online il sito da solo con GitHub Pages.

## Le impostazioni che lo tengono in piedi

**Su GitHub** — Settings → Pages: sorgente *Deploy from a branch*, ramo `main`,
cartella `/ (root)`; dominio personalizzato `impagina.me`; *Enforce HTTPS* attivo.

**Su Register.it** — nella gestione DNS del dominio:

| Tipo | Host | Valore |
|------|------|--------|
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| AAAA | `@` | `2606:50c0:8000::153` |
| AAAA | `@` | `2606:50c0:8001::153` |
| AAAA | `@` | `2606:50c0:8002::153` |
| AAAA | `@` | `2606:50c0:8003::153` |
| CNAME | `www` | `andreablasi71-stack.github.io.` |

I nameserver restano quelli di Register (`ns1` e `ns2.register.it`): si modificano solo
i record dentro la zona.

## Verificare che tutto risponda

```bash
nslookup impagina.me
curl -I https://impagina.me
curl -I https://www.impagina.me
```