# Axiado Corporation

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
