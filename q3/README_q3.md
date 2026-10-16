# Q3: LLM triage of ESG messages (BUS5001 Assessment 3)

Original prompt versus a revised prompt with a strict JSON schema, run through the Google Gemini API from Google Colab, and compared with a rule-based baseline and a Hugging Face zero-shot model (facebook/bart-large-mnli).

Files
- `q3_triage.ipynb`: the Colab notebook, saved with its outputs
- `q3_prompts.json`: original prompt, revised system prompt, JSON schema, test messages and reference labels
- `q3_run_log.json`: every model call with time, model, temperature and raw output
- `q3_parsed_results.json`: parsed records and schema or taxonomy problems for each call
- `q3_baseline_comparison.csv`: reference labels against the four methods, per message
- `q3_consistency.csv`: stability of category, urgency and team across repeats
- `q3_format_reliability.csv`: calls that parsed and calls fully on the allowed values
- `q3_bias_probe.csv`: same fact written in three styles, two repeats each

Notes: temperature 0.5. M1 and M2 ran on gemini-3.8-flash and the remaining messages and the bias probe on gemini-3.5-flash-lite, because the free tier cap of 20 requests per day was reached. The model is stored on every row of the log. Five test messages only, so the comparison is a prototype and not a reliable accuracy estimate.
