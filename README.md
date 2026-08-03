# Axiado Corporation

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Axiado Corporation is a San Jose, California semiconductor company building hardware-anchored, AI-driven platform security for AI data centers, cloud infrastructure, 5G networks and disaggregated compute. Its Trusted Control/Compute Unit (TCU) — the AX3000 family and second-generation AX3080 — integrates the baseboard management controller (BMC), hardware root of trust, TPM, HSM, firewall and LAN-on-motherboard into a single SoC with on-die AI/ML engines. Axiado also ships OCP DC-SCM secure control modules (Smart-SCM3002, SCM3003, SCM3080-MT).

## API surface

Axiado publishes **no hosted public web API and no OpenAPI definition**. The documented API surface is:

- **SecureStack ADK** — an embedded C/C++ SDK for the TCU Secure Enclave (hardened Zephyr RTOS 3.0.0, ARM Cortex-M55), with a full public API reference covering crypto, key management, X.509, BMC control, flash, SPI, DMA, register access and an OS abstraction layer. Source is distributed by Axiado customer engineering.
- **On-device management** — OpenBMC on the TCU, with DMTF Redfish (RESTful API), out-of-band management, KVM redirection and virtual media.

## Links

- Website — https://axiado.com/
- Developer hub — https://devhub.axiado.com/
- API reference — https://devhub.axiado.com/reference
- GitHub — https://github.com/axiado
- News — https://axiado.com/news/

## Artifacts in this repo

| Path | What |
|---|---|
| `llms/` | `llms.txt` harvested verbatim from the developer hub |
| `errors/` | the published `AX_STATUS` registry — 98 codes across 7 modules |
| `conventions/` | ADK engine model, error envelope, async + versioning signals, privilege modes |
| `authentication/` | application-privilege model, firmware image signing, hardware root of trust |
| `conformance/` | OCP DC-SCM 2.0, Redfish, OpenBMC, TPM, Zephyr, DICE — with evidence |
| `lifecycle/` | versioning, and the honest absences (no status page, no deprecation policy, no changelog entries) |
| `packages/` | SecureStack ADK; zero results across npm/PyPI/crates.io/RubyGems |
| `security/` | probed TLS/HSTS/DNSSEC/CAA/SPF/DMARC posture |
| `well-known/` | probe record — no `/.well-known/` document published on any host |
