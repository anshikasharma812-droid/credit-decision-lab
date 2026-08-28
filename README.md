# Credit Decision Lab — V2

Interactive public-data portfolio case study demonstrating how credit-model outputs become operating risk decisions.

## V2 additions

1. **Expected-loss / unit-economics policy optimizer**
   - Adjustable exposure (EAD), loss given default (LGD), and contribution from a performing account.
   - Searches candidate PD thresholds and identifies the illustrative economically preferred cutoff.
   - Makes explicit that model accuracy alone does not determine policy.

2. **Calibration**
   - Holdout accounts are sorted into predicted-risk deciles.
   - Compares average predicted probability of default with observed default rate.
   - Reinforces the distinction between ranking power and probability calibration.

3. **Executive Risk Strategy Recommendation**
   - Converts the selected threshold and economics into a concise operating recommendation.
   - Explicitly calls out validation, fairness, segment stability, sensitivity analysis, vintage monitoring, and champion/challenger rollout before production use.

The original V1 threshold lab, portfolio segmentation, model-driver view, and hypothetical-account sandbox remain included.

## Run locally

From this folder:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deployment

Static site: suitable for GitHub Pages, Netlify, Vercel, or Cloudflare Pages.

## Data

Yeh, I-Cheng (2009), **Default of Credit Card Clients**, UCI Machine Learning Repository.
DOI: 10.24432/C55S3H. License: CC BY 4.0.

Runtime CSV mirror:
`https://raw.githubusercontent.com/thomasXwang/UCI-Credit-card-defaults/master/UCI_Credit_Card.csv`

## Important framing

This is an independent educational portfolio project using public data. It is not employer work, is not a production underwriting model, and should not be represented as such.
