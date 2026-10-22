# Dataset Description: Spaceship Titanic

The CSV files in this folder come from the Kaggle **Spaceship Titanic** competition and are excluded from Git (see the root `.gitignore`). To use them, download the data from the competition page and place the files in this folder:

https://www.kaggle.com/competitions/spaceship-titanic/data

Using the Kaggle CLI:

```bash
kaggle competitions download -c spaceship-titanic
unzip spaceship-titanic.zip -d data/
```

## Files

| File | Approx. rows | Description |
|------|--------------|-------------|
| `train.csv` | ~8,700 | Personal records for about two-thirds of the passengers, used as training data. Includes the target column `Transported`. |
| `test.csv` | ~4,300 | Personal records for the remaining one-third of the passengers. The task is to predict `Transported` for these passengers. |
| `sample_submission.csv` | ~4,300 | Example submission file in the correct format. |

## Columns in `train.csv` and `test.csv`

| Column | Description |
|--------|-------------|
| `PassengerId` | Unique ID for each passenger, in the form `gggg_pp`, where `gggg` is the group the passenger is travelling with and `pp` is their number within the group. People in a group are often family members, but not always. |
| `HomePlanet` | The planet the passenger departed from, typically their planet of permanent residence. |
| `CryoSleep` | Whether the passenger chose to be put into suspended animation for the voyage. Passengers in cryosleep are confined to their cabins. |
| `Cabin` | The cabin the passenger is staying in, in the form `deck/num/side`, where `side` is `P` for Port or `S` for Starboard. |
| `Destination` | The planet the passenger will be debarking to. |
| `Age` | The age of the passenger. |
| `VIP` | Whether the passenger paid for special VIP service during the voyage. |
| `RoomService`, `FoodCourt`, `ShoppingMall`, `Spa`, `VRDeck` | Amount the passenger has billed at each of the ship's luxury amenities. |
| `Name` | The first and last names of the passenger. |
| `Transported` | **Target.** Whether the passenger was transported to another dimension (`True` or `False`). Only present in `train.csv`. |

## Notes

- `test.csv` has the same columns as `train.csv` except `Transported`.
- Many columns contain missing values (roughly 2% per column in the training set).
- `PassengerId` and `Cabin` each pack several pieces of information into one field (group and position, and deck, number and side respectively).

## `sample_submission.csv`

| Column | Description |
|--------|-------------|
| `PassengerId` | ID of each passenger in the test set |
| `Transported` | Predicted target: `True` or `False` |