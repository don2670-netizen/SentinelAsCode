# SD as Code – Sentinel & Defender as Code

Dette repository vedligeholdes af **SocHub**. Hver kundes Microsoft Sentinel- og Defender XDR-konfiguration ligger her som YAML,
og hver ændring – oprettet, ændret eller slettet, i SocHub eller direkte i portalerne – bliver til et commit.
`git log` er dermed den fulde, reviderbare historik, og repoet kan bruges uden SocHub.

## Struktur

```
<Kunde> (<tenant-id>)/
  README.md
  Sentinel/<workspace>/<Type>/<navn>_<id>.yml     Analytics rules, Automation rules, Watchlists, Workbooks …
  Defender/<Type>/<navn>_<id>.yml                  Custom detections, Indicators …
  _deleted/…                                        slettede objekter (kan gendannes)
```

## Versioner og gendannelse

- Historik for ét objekt: `git log -p -- "<Kunde> (<tenant-id>)/Sentinel/<workspace>/Analytics rules/<fil>.yml"`
- I SocHub: **SD as Code** → vælg objektet → *Versioner* → *Gendan denne version*. Gendannelsen sendes til kunden og committes her.

Filer i kundemapperne skrives af SocHub; ændringer skal laves i SocHub eller i portalen, ikke direkte her.
