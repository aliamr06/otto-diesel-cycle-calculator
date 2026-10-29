# Otto & Diesel Cycle Calculator

A responsive browser-based calculator for ideal air-standard Otto and Diesel cycles, with interactive P-v and T-s charts.

## Features
- Otto and Diesel cycle selection
- Enter known state pressures, temperatures, compression ratio, and Diesel cut-off ratio
- `0` means unknown
- Calculates uniquely determinable state properties
- Reports heat supplied, heat rejected, net work, and thermal efficiency when the four state temperatures are known
- Interactive pressure-specific-volume and temperature-entropy plots
- Input validation and inconsistent-input warnings
- No build step required

## Run locally
Open `index.html` in a modern browser. An internet connection is needed for Chart.js, which is loaded from jsDelivr.

## Publish with GitHub Pages
1. Create a repository on GitHub, for example `otto-diesel-cycle-calculator`.
2. Upload `index.html` and `README.md` to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the `main` branch and `/ (root)`, then save.
6. Wait for the deployment to finish. GitHub will show the published URL in the Pages section.

## Model and assumptions
Constant specific heats: `Cp = 1.005 kJ/(kg·K)`, `Cv = 0.718 kJ/(kg·K)`, `k = Cp/Cv`. Pressures are absolute kPa and temperatures are kelvin. The diagrams and results use an ideal air-standard model and should be treated as educational estimates, not real-engine predictions.

## Limitations
The solver uses log-linear state relations and can recover uniquely determined variables from many combinations of state inputs. Heat inputs can help infer state temperatures when the relevant reference temperature is known. The model does not solve every possible nonlinear inverse problem, and insufficient or inconsistent inputs may remain unresolved.
