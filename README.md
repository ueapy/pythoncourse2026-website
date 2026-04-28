# Website for Cefas and Aries Python course 2026

https://ueapy.github.io/pythoncourse2026-website/


Steps to generate pages using mkdocs:


1. Create and activate conda environment using environment.yaml

    1st time
    conda env create -f environment.yml

    then
    conda activate mkdocs

2. Generate pages from markdown files and deploy to github as a branch gh-pages

    ```
    mkdocs gh-deploy --clean
    ```

    To generate pages into the _site directory, without pushing to github

    ```
    mkdocs build
    ```

3. Configure GitHub pages for this repo in Settings > Pages

* Build and deployment
  * Branch > gh-pages and /root



