# 🛡️ Prosjekt: "The Sentinel Whisperer" 🌌

Velkommen til den digitale ekvivalenten av en skuff fylt med gamle kabler, men for Microsoft Sentinel. Dette repoet inneholder restene av en presentasjon som forhåpentligvis lærte deg mer enn du glemte.

> "I thought I saw a false positive, but it was just the cloud staring back at me." 
> — Anonym SOC-analytiker kl. 03:14

---

## 🌀 Hva er dette?
Dette repoet er en herlig blanding av faktiske sikkerhetstips og ren, uforfalsket digital støy. Det ble laget for å huse ressurser fra en Microsoft Sentinel-presentasjon, men endte opp med å bli hjemmet til:
* KQL-spørringer som er så avanserte at de av og til finner ting som ikke finnes.
* Logic Apps som har mer personlighet enn mine faktiske kolleger.
* PowerPoint-lysbilder som ble ofret til "The Demo Gods".



---

## 🛠 Innhold (The Useful Stuff™)
Her inne finner du (kanskje):
1.  **`/Hunting-Queries`**: KQL-magi som kan finne en nål i en høystakk, forutsatt at nålen er tagget med `resourceGroup: 'Security'`.
2.  **`/Playbooks`**: Automatiseringer som gjør jobben din mens du ser på kattevideoer (eller i det minste henter kaffe).
3.  **`/Presentations`**: PDF-versjonen av lysbildene – perfekt for å kurere søvnløshet eller imponere sjefen med grafer som peker oppover.

---

## 💾 Gibberish Metadata (For SEO og Forvirring)
`0xDEADBEEF` | `Cloud_Inception_Final_v2_REAL.ps1` | `sudo make-me-a-sandwich` | `Log_Analytics_is_just_Excel_with_an_ego`

```kql
// En spørring for å finne meningen med livet (eller bare 404-feil)
AzureDiagnostics
| where TimeGenerated > ago(42d)
| extend MeaningOfLife = (21 * 2)
| project MeaningOfLife, Message = "Ingen trusler funnet, bare støv."
