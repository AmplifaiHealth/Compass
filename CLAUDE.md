# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**COMPASS** is a proprietary clinical decision support framework for the NUR Platform by Amplifai Health. It is documentation-only — no build system, package manager, or tests exist.

**Files:**
- `COMPASS_Framework.html` — Single-page interactive reference document (Chart.js v4.4.1 via CDN, dark theme, sidebar nav)
- `Thermal_Asymmetry_Framework.docx` — Supplementary thermography methodology documentation

## Framework Architecture

COMPASS combines two independent data sources into a unified risk score (0–100) and zone assignment:

| Input | Source | What it measures |
|-------|--------|-----------------|
| Systemic Readiness (0–100) | Wearables (HRV, sleep, resting HR, ACWR) | Full-body fatigue/recovery state |
| Thermal Asymmetry Index | Thermography camera | Contralateral tissue inflammation/local stress |

### Four-Zone Classification (Two-Axis Matrix)

| Zone | Score | Systemic | Thermal | Clinical Response |
|------|-------|----------|---------|-------------------|
| Safe | 76–100 | Clear | Clear | Full training load |
| Recovery | 51–75 | Fatigued | Clear | Reduce volume |
| Deceptive Readiness | 26–50 | Ready | Inflamed | Modified load + physio assessment |
| Danger | 0–25 | Fatigued | Inflamed | Mandatory clinical intervention |

"Deceptive Readiness" is the highest-priority zone — athlete feels ready but tissue is stressed, making it the most injury-prone state.

### HTML Document Structure (sections in order)

- **01–05B**: Core philosophy, zone framework, zone meanings, personalisation, asymmetry classification methods (population-based vs. individual SD baseline)
- **06–06.4**: Temporal fusion strategy and signal availability matrix
- **07–10**: CDSS recommendations, zone trajectory over time, clinical practice guidance, implementation
- **Appendix A**: Scientific evidence base

### Asymmetry Classification (Section 05)

Two parallel methods are documented:
- **05A — Population-Based**: Flags asymmetry above a fixed population threshold
- **05B — Individual Baseline SD**: Flags deviation from the athlete's own historical baseline (preferred for longitudinal monitoring)
