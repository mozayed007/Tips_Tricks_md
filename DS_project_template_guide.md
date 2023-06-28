- # Data Science Project Template Guide

  This guide provides a detailed explanation of how to use the Data Science Project Template available at [khuyentran1401/data-science-template](https://github.com/khuyentran1401/data-science-template/tree/dvc-poetry). The template incorporates best practices for structuring a data science project, making it maintainable and reproducible.

  ## Getting Started

  To get started with the template, you first need to install `cookiecutter`:

  ```bash
  pip install cookiecutter
  ```

  Then, you can download the template using the following command:

  ```bash
  cookiecutter https://github.com/khuyentran1401/data-science-template --checkout dvc-poetry
  ```

  You will be prompted to enter some details about your project, and a project with the specified name will be created in your current directory.

  ## Project Structure

  The project structure is organized into several directories, each serving a specific purpose:

  1. **src (Source code):** This folder contains the main Python scripts for the project. It typically includes code related to data gathering, data preparation, feature extraction, model training, and evaluation. Each of these tasks could have a separate Python script or module. This organization allows for code reusability and better understanding of the project's workflow.

  2. **tests:** This directory contains unit tests for the code in the `src` directory. These tests help ensure that the code is functioning as expected and can catch potential bugs or errors. This is an essential part of any software development process, including data science projects.

  3. **models:** This directory is used to store trained machine learning models. The model names could be set as `projectname_date_time` or `project_build_id` to keep track of different versions of the models. This is especially useful when you are experimenting with different models or model parameters.

  4. **data:** This directory contains all the data used in the project. It is typically divided into `raw`, `interim`, `processed`, and `external` subdirectories:
      - `raw`: Stores the original, immutable data dump.
      - `interim`: This is where intermediate data that has been transformed goes.
      - `processed`: This directory holds the final, canonical data sets for modeling.
      - `external`: Stores external data, such as data from third-party sources.

  5. **notebooks:** The `notebooks` directory is used for Jupyter notebooks. These notebooks allow for interactive data analysis with Python and can include descriptions, live code, equations, and visualizations. They are often used for exploratory data analysis, data cleaning and transformation, statistical modeling, data visualization, machine learning, and reporting results.

  6. **reports:** This directory is used for storing outputs of the project like figures, tables, and other reporting artifacts. It helps to keep all generated reports in one place for easy access and review.

  ## Code Quality Control with Pre-commit

  The template uses `pre-commit` to automate the process of checking Python code before committing. This includes checking for a consistent style guide, including docstrings, and more. The hooks executed by `pre-commit` are specified in the `.pre-commit-config.yaml` file.

  To install the pre-commit hooks, run:

  ```bash
  pre-commit install
  ```

  Now, whenever you run `git commit`, your code will be automatically checked and reformatted before being committed.

  ## API Documentation with Pdoc

  The template uses `pdoc` to automatically generate API documentation based on the docstrings of your Python files and objects. To generate the documentation, run:

  ```bash
  make docs
  ```

  The documentation is saved as Markdown files and can be accessed by opening `http://localhost:8080` in your web browser.

  ## Conclusion

  With this guide, you now have a good understanding of how to use the Data Science Project Template to structure your data science projects. The template is designed to be flexible, so feel free to adjust it based on your applications. Happy coding!

  ## References
  - [How to structure a data science project for readability and transparency](https://mathdatasimplified.com/2023/06/17/how-to-structure-a-data-science-project-for-readability-and-transparency-2/)
  - [Data Science Project Template on GitHub](https://github.com/khuyentran1401/data-science-template/tree/dvc-poetry)
  - [Data Science Project Folder Structure](https://dzone.com/articles/data-science-project-folder-structure)
  - [Folder Structure Conventions](https://github.com/kriasoft/Folder-Structure-Conventions/blob/master/README.md)