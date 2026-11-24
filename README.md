# Voltaire Bondoc

I build and break practical defenses against phishing and scams, with a focus on
**private, local AI**: security tools where your browsing never leaves your own hardware.

**What I work on**
- AI-assisted phishing detection that runs on hardware I control, not a cloud service
- Adversarial testing: blind red-team rounds and live phishing pages, not just test suites
- Defense in depth: how browser warnings, DNS filtering, hosting takedowns and on-device
  judgment overlap, and where the gaps are

## Projects

### [Safari Script Observer](https://github.com/bondocai/safari-script-observer) *(open source, MIT; in active development)*
A Safari extension that has a self-hosted LLM judge each page as you browse, and holds the
risky moments (typing a password or card number, downloads, commands copied to the
clipboard) until the model decides. Page contents go only to a model server you own.

- **Blind red-team testing:** 76 attack and look-alike scenarios written by testers who never
  saw the code, across three rounds. Attacks stopped went from 12/14 to 13/14 as fixes
  landed; false alarms on legitimate look-alikes dropped from 4/10 to 2/12.
- **Live phishing test:** 6 of 6 live phishing pages that reached the extension were blocked,
  4 of them before any other layer (browser warnings, DNS filtering, hosting takedowns) had
  caught them.
- **Hardening found by testing:** sealed in-page warnings a page script can't press or remove,
  safe in-memory archive inspection (zip bombs, crafted archives), fail-closed behavior when
  the model can't be reached, and fixes for two bugs that only live phishing exposed.

## Contact
[LinkedIn](https://www.linkedin.com/in/voltaire-bondoc-866286286/)

*Built with AI assistance (Claude); the threat modeling, testing and security decisions are my own.*
