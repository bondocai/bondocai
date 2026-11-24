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

- **Blind red-team testing:** 100 attack and look-alike scenarios written by testers who never
  saw the code, across four rounds, the last aimed at the AI itself (prompt injection). The
  current version stops 55 of 56 attacks and lets 42 of 44 legitimate pages through.
- **Live phishing test:** 6 of 6 live phishing pages that reached the extension were blocked,
  4 of them before any other layer (browser warnings, DNS filtering, hosting takedowns) had
  caught them.
- **Hardening found by testing:** sealed in-page warnings a page script can't press or remove,
  safe in-memory archive inspection (zip bombs, crafted archives), fail-closed behavior when
  the model can't be reached or a page breaks its own check, and fixes for two bugs that
  only live phishing exposed.

## Writing
- [I let an AI on my own hardware guard my browser. Then I threw live phishing at it.](https://www.linkedin.com/pulse/i-let-ai-my-own-hardware-guard-browser-threw-live-phishing-bondoc-npf5e/)

## Contact
[LinkedIn](https://www.linkedin.com/in/voltaire-bondoc-866286286/)

*Built with AI assistance (Claude); the threat modeling, testing and security decisions are my own.*
