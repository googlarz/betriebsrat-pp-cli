# betriebsrat

**Know your rights at work — for employees and works council members.**

> **[🇩🇪 Deutsche Version weiter unten](#deutsch)**

German labour law is full of rights most people don't know they have. This tool makes them instantly accessible — in plain language, in German or English, without needing to know any law yourself.

---

## What can I ask?

Just describe your situation in your own words. Some examples:

**As an employee:**
- "I received a dismissal notice. Was the works council properly consulted?"
- "My employer is restructuring — what am I entitled to?"
- "What is a Betriebsrat and what can it do for me?"
- "I was transferred to a different location without my agreement. Is that allowed?"
- "Can I get severance? I've worked here 7 years and earn €3,500 a month."
- "I'm pregnant and my employer wants to end my contract."
- "My employer introduced monitoring software. Did the works council have to agree?"

**As a works council member:**
- "We received a dismissal hearing notice. What must we do and by when?"
- "The employer wants to introduce an AI writing assistant. Do we have co-determination rights?"
- "We're facing a mass layoff of 20 people. What's our role?"
- "Can we force a Sozialplan if the employer refuses to negotiate?"
- "We want to negotiate a remote work agreement. Where do we start?"

---

## How to get it

Tell Claude to install it:

> Install this: https://github.com/googlarz/betriebsrat

Claude will handle the rest. Then just describe your situation and ask away.

---

## What it knows

- Every paragraph of the *Betriebsverfassungsgesetz* (BetrVG) — the German works constitution law
- Co-determination rights: when the works council can block, must consent, or is only informed
- Legal deadlines — including the critical **3-week window** to challenge a dismissal in court
- Sozialplan and severance calculations (Munich formula)
- AGG (discrimination), Mutterschutz (maternity), Elternzeit (parental leave), SGB IX (disability)
- Procedure violations — what happens if the employer didn't follow the rules

---

## License

Apache 2.0 — see [LICENSE](LICENSE).

*This tool provides legal orientation, not legal advice. For your specific situation, consult a labour law specialist or your trade union.*

---

<details>
<summary>For developers — CLI reference</summary>

### Install (CLI)

```bash
go install github.com/googlarz/betriebsrat/cmd/betriebsrat@latest
betriebsrat doctor
```

### Key commands

```bash
betriebsrat ask "Ich wurde entlassen. Was nun?"
betriebsrat rights-check "KI-Überwachungssystem einführen" --agent
betriebsrat decide "Massenentlassung 20 Personen" --json
betriebsrat sozialplan-calc --salary 3500 --years 7
betriebsrat nachteilsausgleich --salary 3500 --years 7 --no-ia-attempted
betriebsrat check-anhoerung "<text des Anhörungsschreibens>"
betriebsrat deadline kuendigung --from 2026-05-10
betriebsrat law 102
betriebsrat bv-template homeoffice
betriebsrat ki-check "Teams-Analysefunktion zur Produktivitätsmessung"
betriebsrat massenentlassung --employees 120 --affected 25
```

### MCP server

```bash
# Claude Code
claude mcp add betriebsrat betriebsrat-pp-mcp

# Claude Desktop
{
  "mcpServers": {
    "betriebsrat": { "command": "betriebsrat-pp-mcp" }
  }
}
```

### Output flags

`--json` · `--agent` · `--lang en` · `--lang de`

</details>

---

---

<a name="deutsch"></a>

# betriebsrat — Deutsche Dokumentation

**Arbeitsrechte kennen — für Arbeitnehmer und Betriebsratsmitglieder.**

Das deutsche Arbeitsrecht steckt voller Rechte, von denen die meisten Menschen nichts wissen. Dieses Tool macht sie sofort zugänglich — in einfacher Sprache, auf Deutsch oder Englisch, ohne dass Sie selbst Jura studiert haben müssen.

---

## Was kann ich fragen?

Beschreiben Sie Ihre Situation einfach in Ihren eigenen Worten. Ein paar Beispiele:

**Als Arbeitnehmer:**
- „Ich habe eine Kündigung erhalten. Wurde der Betriebsrat ordnungsgemäß angehört?"
- „Mein Arbeitgeber restrukturiert den Betrieb — was steht mir zu?"
- „Was ist ein Betriebsrat und was kann er für mich tun?"
- „Ich wurde ohne mein Einverständnis versetzt. Ist das erlaubt?"
- „Habe ich Anspruch auf eine Abfindung? Ich arbeite hier seit 7 Jahren und verdiene 3.500 € monatlich."
- „Ich bin schwanger und mein Arbeitgeber will meinen Vertrag beenden."
- „Mein Arbeitgeber hat eine Überwachungssoftware eingeführt. Musste der Betriebsrat zustimmen?"

**Als Betriebsratsmitglied:**
- „Wir haben ein Anhörungsschreiben für eine Kündigung erhalten. Was müssen wir tun und bis wann?"
- „Der Arbeitgeber will einen KI-Schreibassistenten einführen. Haben wir ein Mitbestimmungsrecht?"
- „Uns droht eine Massenentlassung von 20 Personen. Was ist unsere Rolle?"
- „Können wir einen Sozialplan erzwingen, wenn der Arbeitgeber nicht verhandeln will?"
- „Wir wollen eine Homeoffice-Regelung aushandeln. Wo fangen wir an?"

---

## Wie bekomme ich das Tool?

Sagen Sie Claude, es soll installieren:

> Install this: https://github.com/googlarz/betriebsrat

Claude übernimmt den Rest. Dann beschreiben Sie einfach Ihre Situation.

---

## Was das Tool weiß

- Alle Paragrafen des Betriebsverfassungsgesetzes (BetrVG)
- Mitbestimmungsrechte: wann der Betriebsrat blockieren kann, zustimmen muss oder nur informiert wird
- Gesetzliche Fristen — einschließlich der kritischen **3-Wochen-Frist** für die Kündigungsschutzklage
- Sozialplan- und Abfindungsberechnungen (Münchner Formel)
- AGG (Diskriminierungsschutz), Mutterschutz, Elternzeit (BEEG), SGB IX (Schwerbehinderung)
- Verfahrensfehler — was passiert, wenn der Arbeitgeber die Regeln nicht eingehalten hat

---

## Lizenz

Apache 2.0 — siehe [LICENSE](LICENSE).

*Dieses Tool bietet rechtliche Orientierung, keine Rechtsberatung. Für Ihren konkreten Fall wenden Sie sich an einen Fachanwalt für Arbeitsrecht oder Ihre Gewerkschaft.*

---

<details>
<summary>Für Entwickler — CLI-Referenz</summary>

### Installation (CLI)

```bash
go install github.com/googlarz/betriebsrat/cmd/betriebsrat@latest
betriebsrat doctor
```

### Wichtige Befehle

```bash
betriebsrat ask "Ich wurde entlassen. Was nun?"
betriebsrat rights-check "KI-Überwachungssystem einführen" --agent
betriebsrat decide "Massenentlassung 20 Personen" --json
betriebsrat sozialplan-calc --salary 3500 --years 7
betriebsrat nachteilsausgleich --salary 3500 --years 7 --no-ia-attempted
betriebsrat check-anhoerung "<text des Anhörungsschreibens>"
betriebsrat deadline kuendigung --from 2026-05-10
betriebsrat law 102
betriebsrat bv-template homeoffice
betriebsrat ki-check "Teams-Analysefunktion zur Produktivitätsmessung"
betriebsrat massenentlassung --employees 120 --affected 25
```

### Ausgabeformate

`--json` · `--agent` · `--lang en` · `--lang de`

</details>
