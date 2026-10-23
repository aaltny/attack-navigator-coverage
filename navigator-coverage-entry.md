# attack-navigator-coverage — Technique Entry

## Tablo Satırı (coverage tablosu için)

| Tactic | Technique ID | Technique Name | Sub-technique | Kaynak Alert (rule.id) | Durum |
|---|---|---|---|---|---|---|
| Credential Access | T1110 | Brute Force | T1110.001 (Password Guessing) | 60122, 92652 | Covered (lab-simulated) |

**Not:** Wazuh'un kendi `rule.mitre` etiketi (`T1531`, Impact taktiği) bu satırla **uyuşmuyor** — bilinçli olarak manuel düzeltme yapıldı, gerekçe README'de.

## Navigator Layer'ında İşaretlenecekler

1. [ATT&CK Navigator](https://mitre-attack.github.io/attack-navigator/) üzerinde **Enterprise ATT&CK** matrisini aç.
2. **Credential Access** taktiği altında **T1110 (Brute Force)** hücresini bul.
3. Alt-teknik olarak **T1110.001 (Password Guessing)** seç.
4. Score/renk: "Covered — Simulated" anlamına gelecek şekilde işaretle (ör. yeşil, score: 1), metadata alanına şunu ekle:
   ```
   comment: "Lab-simulated: single-account SMB brute-force via NetExec, detected by Wazuh rule 60122/92652. Wazuh default MITRE tag (T1531) was incorrect — manually corrected to T1110.001 after review."
   ```
5. Layer'ı `.json` olarak export et, `attack-navigator-coverage` reposuna commit et.
6. **Export etmeden önce:** layer JSON içinde gerçek IP/hostname geçmediğinden emin ol (bu teknik için normalde geçmez, ama comment alanını kontrol et).
