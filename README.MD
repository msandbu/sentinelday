# 🛡️ Prosjekt: "The Sentinel Whisperer" 🌌

Velkommen til et repo som ser ut som en intern wiki etter tre espresso og ett incident bridge-møte for mye. Her bor ikke bare minner fra en Sentinel-presentasjon – her bor også en liten armé av etterforsknings-workflows.

> "Vi hadde én alert. Nå har vi 14 dashboards, 3 hypoteser og en eksistensiell krise."  
> — Anonym SOC-analytiker, sannsynligvis tirsdag

---

## 🌀 Hva er dette?
Kortversjon: Et sikkerhetsfokusert arbeidsområde for Microsoft Sentinel + Defender XDR, pakket inn i nok humor til at SIEM-traumer føles litt mindre personlige.

Langversjon: Dette repoet er bygget rundt GitHub Copilot-instruksjoner, ferdige skill-workflows og prompts for undersøkelser, triage, KQL-authoring og visualisering.

---

## 🛠 Innhold (The Useful Stuff™)
Det som faktisk finnes her (ingen clickbait):

1. **`.github/copilot-instructions.md`**  
	Den store regelboka™ for hvordan undersøkelser skal kjøres: workspace-valg, KQL pre-flight checks, evidenskrav, output-format og anti-hallusinasjon-regler.

2. **`.github/skills/`**  
	Ferdige etterforskningspakker for blant annet:
	- `user-investigation`, `computer-investigation`, `incident-investigation`, `ioc-investigation`
	- `authentication-tracing`, `ca-policy-investigation`
	- `kql-query-authoring`, `detection-authoring`, `mcp-usage-monitoring`
	- `honeypot-investigation`, `exposure-investigation`, `sentinel-ingestion-report`
	- `geomap-visualization`, `heatmap-visualization`
	- `scope-drift-detection` (`device`, `spn`, `user`)

3. **`.github/prompts/`**  
	Promptbibliotek for ulike domener (`cloud`, `email`, `endpoint`, `identity`, `network`) + raskere analyser av alert-evidence.

---

## 🧪 Hvordan bruke dette repoet uten å gråte
- Åpne en skill under `.github/skills/<skill>/SKILL.md` når du har en konkret investigation-type.
- Følg `copilot-instructions.md` før ad-hoc KQL, spesielt når du er fristet til å "bare kjøre en rask query".
- Bruk prompts i `.github/prompts/` når du trenger struktur i stedet for improvisert SOC-poesi.

---

## 💾 Gibberish Metadata (For SEO og Forvirring)
`0xDEADBEEF` | `FalsePositive_Or_ExistentialDread.ps1` | `where CoffeeLevel > 9000` | `KQL_is_SQL_after_dark`

```kql
// Vi sjekker om universet fortsatt er on fire
SecurityAlert
| where TimeGenerated > ago(7d)
| summarize Alerts = count() by ProviderName
| order by Alerts desc
```
