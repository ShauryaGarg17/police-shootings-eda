# Dataset

The notebook expects a local CSV named `shootings.csv`, uploaded interactively in Google Colab.

**The original dataset is not included in this repository package.** Obtain the dataset from the original course/provider source and verify that you have permission to redistribute it before committing it publicly.

The uploaded CSV used in the recorded analysis contained approximately 4,898 rows and 15 original columns, including `id`, `name`, `date`, `manner_of_death`, `armed`, `age`, `gender`, `race`, `city`, `state`, `signs_of_mental_illness`, `threat_level`, `flee`, `body_camera`, and `arms_category`.

To run: open the notebook in Colab, run the upload cell, and choose your `shootings.csv`.

The `.gitignore` excludes `data/*.csv` to prevent accidental publication of data. If you have redistribution rights and want to include the CSV, remove that ignore rule deliberately.
