# MPH Thesis Template

This repository provides a simple and customizable template to write a **Master of Public Health (MPH) thesis** using [Quarto](https://quarto.org/), created for students at **Sree Chitra Tirunal Institute for Medical Sciences and Technology (SCTIMST), Trivandrum**. It is designed to generate a polished PDF document with all standard thesis sections and formatting requirements.

## Getting Started

Follow the steps below to set up and use the template:

1.  **Install Quarto** Download and install Quarto from [https://quarto.org](https://quarto.org/).

2.  **Clone or Download the Repository** You can clone the repository using Git or download it as a ZIP file and extract it.

3.  **Open the Project** Open the project folder in [RStudio](https://posit.co/download/rstudio/) (recommended) or any text editor of your choice.

4. **Edit the Content**

   - Draft your thesis using the `.qmd` (Quarto Markdown) files provided in the template. Each file corresponds to a section of your thesis, such as `abstract.qmd`, `introduction.qmd`, `methods.qmd`, etc.

   - Use [Quarto’s official guide](https://quarto.org/docs/guide/) for help with formatting text, adding citations, inserting figures, and structuring chapters. It provides detailed instructions on using code chunks, cross-references, equations, and more.

   - Add your **Acknowledgements** section in `index.qmd`.
     ⚠️ Note: `index.qmd` is required for Quarto to identify the starting point of the document. The rendering will fail if this file is missing.

   - Customize your **Title Page** by editing the `titlepage.tex` file. Update fields such as the title, author name and year as needed.

5.  **Insert Figures and Attachments** Place all images, diagrams, and other supplemental materials in the `attachments/` folder. Link them from within `.qmd` files using the relative path, e.g.:

    ``` markdown
    ![](attachments/my_figure.png)
    ```

6.  **Add Bibliography**

    -   Export your reference library from Zotero as a `references.bib` file (see steps below).
    -   Place `references.bib` in the project directory.

7.  **Set Citation Style**

    -   The template uses the **SAGE Harvard** citation style (`sage-harvard.csl`) by default.
    -   If you prefer a different style, download a `.csl` file from the [Zotero Style Repository](https://www.zotero.org/styles) and update the `csl` entry in `_quarto.yml`.

## Folder Structure

```         
📁 mph-thesis-template/
├── _output/            # Rendered PDF output
├── _quarto.yml         # Quarto project configuration
├── index.qmd           # Acknowledgements
├── abstract.qmd        # Abstract section
├── introduction.qmd    # Introduction
├── methods.qmd         # Methods
├── results.qmd         # Results
├── discussion.qmd      # Discussion
├── references.bib      # Bibliography file
├── sage-harvard.csl    # Citation style (modifiable)
├── titlepage.tex       # Custom LaTeX title page
├── header.tex          # LaTeX formatting settings
├── attachments/        # Figures and other embedded files
└── sctimst_emblem.png  # SCTIMST emblem for title page
 
```

## Creating `references.bib` from Zotero

You can export your references from Zotero to use with this template:

1.  **Select Items** In Zotero, select the collection or references you want to include.

2.  **Export** Right-click the selection and choose **Export Collection...** or **Export Items...**.

3.  **Choose Format** In the export dialog, choose `BibTeX` as the format. ⚠️ Make sure **“Keep updated”** is **unchecked** unless you're using an advanced integration.

4.  **Save the File** Save the file as `references.bib` and place it in the root of your project directory.

5.  **Link in `_quarto.yml`** Ensure the following lines are present in your `_quarto.yml` file:

    ``` yaml
    bibliography: references.bib
    csl: sage-harvard.csl
    ```

## Rendering the Thesis

Once your content and references are ready, you can compile your thesis using **Quarto**.

Run the following command in your **terminal** in the project folder (not the R console):

``` bash
quarto render
```

Alternatively, if you're using **RStudio**, you can simply press **Ctrl + Shift + B** (Windows/Linux) or **Cmd + Shift + B** (Mac) to render the entire project.

The final PDF file will be saved in the `_output/` directory.

## License

This project is released under the **MIT License**. See `LICENSE.txt` for details.

Feel free to modify and extend the template to suit your institution’s formatting guidelines or personal preferences. Contributions and suggestions are welcome!
