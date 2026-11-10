LUMAI LIFTING BODY — BASELINE GEOMETRY FOR KIKI
Prepared 10 November 2026 for technical discussion on 11–12 November 2026

Contents
- geometry.json: exact baseline parameter values from the private Lumai GitHub repository (main branch, September 14 2026).
- lifting_body_baseline_sections.stl: watertight triangular surface assembled from the parametric cross sections defined by the repository's src/rfd/geometry.py. This file was constructed independently of OpenVSP and has NOT been compared against the canonical OpenVSP export.

Baseline geometry
- Length: 1.20 m; maximum aft width: 0.65 m.
- Coordinates: x nose-to-aft, y right, z up; ALL dimensions in metres.
- 41 longitudinal cross sections; nose singularity and aft cut capped in the STL.

IMPORTANT LIMITATIONS
- Preliminary geometry only, NOT an aerodynamic design baseline or flight-qualified geometry.
- No defined flaps/elevons, recovery hardware, actuators, internal structure or TPS layers.
- STL is a geometry-review convenience, NOT a validated CFD-ready export or reference mesh. Please check tessellation and independent mesh convergence before CFD.
- No verified hypersonic, transonic or low-speed aero database is enclosed. No stability, controllability, heating or terminal flight claims.
- The original repository contains Modified-Newtonian and heating proxy tools with explicitly limited validity; these are NOT included in this share package.
- If you need an editable OpenVSP-native geometry.vsp3, generate it from the original private repository using OpenVSP 3.51.1 and its setup; see below. That file is NOT in this ZIP.
- This package contains no Git history. Preserve original company records and IP provenance separately.

Original private repository
https://github.com/lumai-tech/lumai-lifting-body
From its root, with the OpenVSP environment set up:
    scripts/setup
    scripts/generate-openvsp configs/geometry.json build/geometry.vsp3
    scripts/generate-analysis-mesh configs/geometry.json configs/aero_mesh.json build/aero_mesh/current/body.stl
The build/ output directory is intentionally gitignored.

Suggested technical review
1. Is the baseline lifting-body shape appropriate for the intended subscale demonstration?
2. Main stability and control-surface gaps across hypersonic / transonic / low-speed regimes?
3. Minimum credible aero/thermal and entry trajectory analyses for an NSIP proposal?
4. Recommend updated geometry, flap arrangements and a test-and-validation sequence.

Confidential — shared for Lumai technical collaboration only. Not for public distribution.
