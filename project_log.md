touch project_log.md

mkdir my_ds_project_revision

cd my_ds_project_revision

git init

touch README.md

echo "# My Data Science Project Revision" > README.md

echo "This project is a hands-on revision of setting up a data science workflow with Git and GitHub." >> README.md

git add README.md

git commit -m "Initial commit: Add README"

git remote add origin https://github.com/machristians/qtm350_5-23_practice.git

git branch -M main

git push -u origin main

mkdir -p data/{raw,processed} notebooks scripts results docs

touch scripts/01_data_preprocessing.py scripts/02_analysis.py notebooks/exploratory_data_analysis.ipynb data/raw/placeholder.txt docs/project_plan.md

echo "## Project Plan" > docs/project_plan.md

echo "1. Setup project structure." >> docs/project_plan.md

echo "2. Implement data preprocessing." >> docs/project_plan.md

echo "3. Perform analysis." >> docs/project_plan.md

touch .gitignore

echo "# Python" >> .gitignore

echo "__pycache__/" >> .gitignore

echo "*.pyc" >> .gitignore

echo "*.pyo" >> .gitignore

echo "*.pyd" >> .gitignore

echo "" >> .gitignore

echo "# Jupyter Notebook" >> .gitignore

echo ".ipynb_checkpoints/" >> .gitignore

echo "" >> .gitignore

echo "# Data files" >> .gitignore

echo "data/raw/*" >> .gitignore

echo "data/processed/*" >> .gitignore

echo "!data/raw/placeholder.txt" >> .gitignore

echo "" >> .gitignore

echo "# Results" >> .gitignore

echo "results/*" >> .gitignore

echo "" >> .gitignore

echo "# Environment" >> .gitignore

echo ".env" >> .gitignore

echo "venv/" >> .gitignore

echo "env/" >> .gitignore

git add .

git commit -m "Feat: Setup project directory structure and gitignore"

git push origin main

git branch feature/add-initial-script-logic

git checkout feature/add-initial-script-logic

echo "# scripts/01_data_preprocessing.py" > scripts/01_data_preprocessing.py

echo "import pandas as pd" >> scripts/01_data_preprocessing.py

echo "" >> scripts/01_data_preprocessing.py

echo "def load_data(filepath):" >> scripts/01_data_preprocessing.py

echo "    print(f\"Loading data from {filepath}...\")" >> scripts/01_data_preprocessing.py

echo "    # df = pd.read_csv(filepath)" >> scripts/01_data_preprocessing.py

echo "    # print(\"Data loaded successfully.\")" >> scripts/01_data_preprocessing.py

echo "    # return df" >> scripts/01_data_preprocessing.py

echo "" >> scripts/01_data_preprocessing.py

echo "print(\"Data preprocessing script initialized.\")" >> scripts/01_data_preprocessing.py

cp data/raw/placeholder.txt data/processed/processed_placeholder.txt

git add scripts/01_data_preprocessing.py data/processed/processed_placeholder.txt

git commit -m "Feat: Add initial logic to preprocessing script and simulate output"

git checkout main

git merge feature/add-initial-script-logic

git branch -d feature/add-initial-script-logic

git push origin main

git add project_log.md

git commit -m "Docs: Add project log with commands"

git push origin main
