# Mellingen – Äbereich (NFA-001)

Project repository for the Mellingen pilot of the Nature Finance Accelerator (NFA).
The project's entry in the NFA Project Register is generated from `nfa-project.json` in this repository:

**https://register.nfa.ch/project.html?id=mellingen**

## What is in here

| Path | Content |
|---|---|
| `nfa-project.json` | The project file: description, measurements, datasets, agreements, organisations, timeline. The only file the register reads. |
| `images/` | Photos shown on the register page. The first entry in `images` is the header photo; with two or more, the page shows an Images section. |
| `logos/` | Partner logos. Add a logo only after the partner has confirmed its use in writing, then set `logoConfirmed` to `true`. |
| `geo/` | Project boundary as `boundary.geojson` (WGS84; source data in CH1903+/LV95, EPSG:2056). |
| `data/` | Small files only. Large datasets go to an open archive (Zenodo, OpenTopography, InfoSpecies) and are linked by DOI in `nfa-project.json`. |

## How to update the entry

1. Edit `nfa-project.json` (on GitHub: open the file, click the pencil, commit).
2. The register picks up the change at its next nightly run, or immediately when someone runs the "Collect projects" workflow in the register repository.
3. Add a line to `changelog` in the project file for every change that matters.

### Common edits

- **A dataset gets a DOI:** set `doi` (e.g. `10.5281/zenodo.1234567`), set `status` to `available`.
- **An agreement is signed:** set `status` to `signed`, fill in `signed` (date), `term`, `dataLicence`, `claimRights`. Set `disclosure` to `public` if the parties agree.
- **A partner confirms logo use:** put the logo in `logos/` (file name as in `nfa-project.json`), set `logoConfirmed` to `true` plus `logoConfirmedOn` to the date. Keep the confirmation itself internal, not in this public repository.
- **A new photo:** put it in `images/` (JPEG, about 2000 px wide, exported without GPS location), add an entry to `images` with `src`, `alt`, `caption`, `date`, `credit`, `licence`. Recognisable people only with their consent.
- **A person agrees to be named:** set `consent` to `true`, add the ORCID.
- **The boundary is ready:** save it as `geo/boundary.geojson`, set `location.boundary` to `geo/boundary.geojson` and `boundaryStatus` to `surveyed`.

### Disclosure levels

| Value | Shown on the register |
|---|---|
| `public` | In full, with link |
| `on-request` | The entry, not the content. Requests go to register@nfa.ch |
| `not-disclosed` | The entry with a one-line `reason` |

Fees are never published.

## Licence

Metadata in this repository: CC BY 4.0 (see `LICENSE`). Datasets carry their own licence, stated per dataset.
