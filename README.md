# zvaka-training

Colab-first training workflow for meal-calorie fine-tuning from a Google Drive
dataset uploaded by the companion ingestion API.

## Files

- `gemma_calorie_finetune.ipynb`: main Colab notebook

## Dataset expectation

The notebook expects a Drive folder containing pairs like:

- `20260416T120102Z-abc123.jpg`
- `20260416T120102Z-abc123.json`

The JSON sidecar is expected to contain:

- `description`
- `calorie_estimate`
- `captured_at`
- `confidence_state`

## Notes

- The notebook is written so the base model id is easy to change. Set it to the
  exact Gemma 4 E2B checkpoint you have access to.
- The notebook exports adapters and the prepared dataset back into Drive.
