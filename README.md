# SD as Code, Sentinel & Defender as Code

Dette repository vedligeholdes af **SOROC**. Hver kundes Microsoft Sentinel- og Defender XDR-konfiguration ligger her som YAML,
og hver ændring, oprettet, ændret eller slettet, i SOROC eller direkte i portalerne, bliver til et commit.
`git log` er dermed den fulde, reviderbare historik, og repoet kan bruges uden SOROC.

## Struktur

```
<Kunde> (<tenant-id>)/
  README.md
  Sentinel/<workspace>/<Type>/<navn>_<id>.yml     Analytics rules, Automation rules, Watchlists, Workbooks …
  Defender/<Type>/<navn>_<id>.yml                  Custom detections, Indicators …
  …/<Type>/_deleted/<navn>_<id>.yml                  slettede objekter ligger i typens egen mappe (kan gendannes)
```

## Versioner og gendannelse

- Historik for et objekt: `git log -p -- "<Kunde> (<tenant-id>)/Sentinel/<workspace>/Analytics rules/<fil>.yml"`
- I SOROC: **SD as Code** → vælg objektet → *Versioner* → *Gendan denne version*. Gendannelsen sendes til kunden og committes her.

Filer i kundemapperne skrives af SOROC; ændringer skal laves i SOROC eller i portalen, ikke direkte her.
