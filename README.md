# British Airways Data Science Job Simulation

Two projects completed through the Forage virtual experience with British Airways (Oct-Nov 2026).

## Task 1: Lounge eligibility model for Heathrow Terminal 3 (Excel)
**Question:** What share of passengers would be eligible for each of three lounge tiers, by type of flight?

**What I did**
- Profiled 10,000 summer departures and kept every row after testing whether repeated flight numbers were true duplicates (they weren't).
- Grouped flights by haul (short or long) and time of day (8 groups), based on seat-mix evidence.
- Built a reusable lookup table with eligibility assumptions in one input sheet (Low / Base / High scenarios).

**Key finding:** Eligibility depends mostly on cabin mix, and the share of frequent-flyer status holders in Economy is the biggest uncertainty.

**Limitation:** Status shares are assumptions, and the dataset's benchmark columns disagree with the model, especially for Tier 1 on long-haul.

## Task 2: Predicting customer bookings (Python)
**Question:** How well can booking details predict whether a customer completes a booking?

**What I did**
- Cleaned 50,000 bookings (removed 719 duplicates), converted text to numbers, and created two features.
- Trained a RandomForest and evaluated it with a held-out test set and 5-fold cross-validation.

**Result:** Accuracy 85%, which is no better than always guessing "no booking" (85%). AUC 0.76, recall 10%. The data has some signal but is only weakly predictive.

**Top drivers:** purchase lead time, route, flight hour, length of stay, booking country.

**Limitation:** Route and booking origin were number-coded, which may overstate their importance.

## Tools
Excel, Python (pandas, scikit-learn, matplotlib), Google Colab.

*The raw datasets are not included. They belong to the Forage program.*
