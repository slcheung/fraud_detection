
# Fraud Statement Detection
----------
Have you ever encountered statements that initially struck you as surprising, but then left you questioning their complete truth?

This mini-project aims to tackle this issue by leveraging the capabilities of Large Language Models (LLMs). Its goal is to analyze a given statement and determine, based on readily available online information, whether it is fraudulent or misleading.


## How to use
-------
* We use Jupyter notebooks for this mini-project, but you can also try it out on [Colab](https://colab.google/)! Here's a breakdown of the functions in each notebook:

| **Notebook** | **Function** |
| ---- | ---- |
| `prompt_dollyv2.ipynb` | This calls the LLM [Dolly-v2 from huggingface](https://huggingface.co/databricks/dolly-v2-3b) for the statement detection.  We played around with the parameters and currently we settled with a set that are in the code right now.  We played around with the prompt as well in order to get a consistent and meaning response from it.  There are some test cases as well in the notebook for testing. |
| `prompt_gemma.ipynb` | This calls the LLM [Gemma from huggingface](https://huggingface.co/google/gemma-2b) for the statement detection.  Ceveat:  it could barely work if use CPU only on colab, but it's better to use GPU resource (T4) for this.  Also, in order to run this model, you might need to get your personal access token from huggingface.  Please checkout [HowTo](https://huggingface.co/docs/hub/en/security-tokens) for details.  There are some test cases as well in the notebook for testing (same as above). |
| `scrape_url_content.ipynb` | This scrapes content from valid URLs via google search.  This returns a table for the statement detection above. |
| `test_scrape_dollyv2.ipynb` | This is a testing example to link both scraping and statement detection above using [Dolly-v2](https://huggingface.co/databricks/dolly-v2-3b). |
| `test_Scrape_gemma.ipynb` | This is a testing example to link both scraping and statement detection above using [Gemma](https://huggingface.co/google/gemma-2b). |
## Get Started
------

0. In Jupyter Notebook, open either `test_scrape_dollyv2.ipynb` or `test_scrap_gemma.ipynb` for a trial.
1. Edit the provided statements and adjust the number of returned valid content entries at the end of each notebook.
2. Feel free to share any suggestions or comments! :)
