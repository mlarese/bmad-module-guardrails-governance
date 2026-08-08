# Guardrails Governance (`grg`)

Tre figure di presidio su privacy e GDPR, legale e licenze, compliance normativa — più un workflow di ricerca live sugli aggiornamenti legali. Separano l'obbligo vero dalla prassi diffusa, e dicono quali norme non si applicano.

Modulo BMad. È una porzione del bundle [Guardrails](https://github.com/mlarese/bmad-module-guardrails):
stesse figure, stesso comportamento, solo l'area governance.

> **Generato.** Questo repository è prodotto da `tools/build_modules.py` nel
> repository [bmad-module-guardrails](https://github.com/mlarese/bmad-module-guardrails).
> Le modifiche si fanno lì e poi si rigenera: qui vengono sovrascritte.

## Figure

| Figura | Ruolo | Skill | Cosa presidia |
| ------ | ----- | ----- | ------------- |
| 🛡️ Vera | Data Protection Officer | `grl-agent-privacy` | Parte sempre dai dati concreti — quali dati personali esattamente, chi li vede, per quanto tempo — e separa l'obbligo GDPR vero dalla prassi diffusa: base giuridica di una… |
| ⚖️ Aldo | Tech Lawyer | `grl-agent-legal` | Traduce licenze open source (GPL, AGPL, MIT), proprietà intellettuale del codice — anche quello generato dall'AI — contratti e DPA con i fornitori, termini di servizio e vincoli… |
| 📐 Nils | Regulatory Compliance | `grl-agent-compliance` | Prima esclude, poi prescrive: delle norme che ti preoccupano, quasi sempre metà non ti riguarda. |

## Skill e workflow

| Skill | Comando | Cosa fa |
| ----- | ------- | ------- |
| `grg-setup` | Installa Guardrails Governance | Registra Guardrails, le tre figure, le stanze tematiche di party mode e le voci di help. Non crea la memoria condivisa. |
| `grg-profile` | Profila il progetto | Raccoglie in pochi minuti gli otto campi che danno contesto a tutte e tre le figure, criticità inclusa. |
| `grg-profile` | Aggiorna il profilo | Riallinea il profilo quando il progetto cambia, e dice se il cambiamento invalida rischi già accettati. |
| `grg-board` | Convoca il collegio | Fa leggere lo stesso artefatto alle sole figure pertinenti e restituisce un riepilogo unico, conflitti compresi. |
| `grg-board` | Rischi già accettati | Mostra, raggruppato per figura, quello che il progetto ha consapevolmente scelto di accettare. |
| `grl-legal-updates` | Ultime novità legali | Recupera leggi, decreti, bollettini, sentenze ed emendamenti nel periodo indicato, con ricerca live, matrice di copertura, lineage di vigenza e due gate bmad-review. |

## Installazione

```
bmad install grg
```

Poi, come primo passo, `grg-profile`: raccoglie il profilo di progetto — settore,
dati trattati, mercato, stack, criticità — e da lì ogni figura deriva quanto essere
severa. Senza profilo il default resta `normal` e le figure partono senza contesto.

## Memoria condivisa

Il profilo vive in `{project-root}/_bmad/memory/grl-shared/project-profile.md`, insieme
a `decisions.md` e `accepted-risks.md`. Il percorso è lo stesso per tutti i moduli
Guardrails: installandone due, il profilo resta uno solo e si compila una volta.

## Convivenza con il bundle

Questo modulo installa skill con **lo stesso nome** del bundle `grl` — `grl-agent-privacy`
sta identica in entrambi. Bundle e moduli tematici non vanno installati insieme nello
stesso progetto: si sceglie il bundle completo, oppure i moduli delle aree che servono.

## Stanze di party mode

grg-setup installa le stanze del modulo in `_bmad/custom/bmad-party-mode.toml`, senza cambiare la stanza di default:

- `bmad-party-mode --party grl-governance`

## Licenza

MIT.
