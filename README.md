# Poznámky z elektrotechniky

Zápisky sú usporiadané tak, aby sa dali pridávať ďalšie hodiny bez straty pôvodného textu.

| Priečinok | Obsah |
| --- | --- |
| [`povodne/`](povodne/) | Bajtovo nezmenené zálohy vstupných súborov |
| [`hodiny/`](hodiny/) | Jednotlivé hodiny s opravenou diakritikou a zvýraznením |
| [`ucivo/`](ucivo/) | Učivo rozdelené podľa tém, s odkazmi na hodiny |
| [`priklady/`](priklady/) | Samostatné príkladové textové súbory, uložené bez zmien mimo poznámok |

## Hodiny

- [Hodina 1: Stavba atómu a vodivosť látok](hodiny/hodina1.md)
- [Hodina 2: Elektrický náboj, napätie a prúd](hodiny/hodina2.md)
- [Hodina 3: Elektrický obvod](hodiny/hodina3.md)
- [Hodina 4: Prúdová hustota a elektrický prúd](hodiny/hodina4.md)
- [Hodina 5: Merný odpor, merná vodivosť](hodiny/hodina5.md)
- [Hodina 6: Ohmov zákon a elektrická vodivosť](hodiny/hodina6.md)
- [Hodina 7: Závislosť odporu od teploty a supravodivosť](hodiny/hodina7.md)

## Učivo

- [Stavba atómu a vodivosť látok](ucivo/01-stavba-atomu-a-vodivost.md)
- [Elektrický náboj](ucivo/02-elektricky-naboj.md)
- [Napätie a prúd](ucivo/03-napatie-a-prud.md)
- [Elektrický obvod](ucivo/04-elektricky-obvod.md)
- [Prúdová hustota](ucivo/05-prudova-hustota.md)
- [Merný odpor a merná vodivosť](ucivo/06-merny-odpor-a-merna-vodivost.md)
- [Ohmov zákon a elektrická vodivosť](ucivo/07-ohmov-zakon-a-elektricka-vodivost.md)
- [Závislosť odporu od teploty a supravodivosť](ucivo/08-zavislost-odporu-od-teploty-a-supravodivost.md)

Nový neupravený súbor pridaj do koreňa repozitára a požiadaj agenta, aby spracoval novú hodinu podľa [AGENTS.md](AGENTS.md). Agent najprv uloží nezmenenú zálohu, potom pripraví verziu v `hodiny/` a doplní `ucivo/`.

Samostatné príkladové textové súbory patria iba do `priklady/` v koreni repozitára. Ich obsah zostáva nezmenený a nezapracúva sa do poznámok ani učiva.

Zjavné nejasnosti pôvodných zápiskov sú uvedené v [NEJASNOSTI.md](NEJASNOSTI.md). Text učiva ich neopravuje bez rozhodnutia autora.
