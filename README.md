# latex-translator

## Setup

### 1. Launch Dev Container

Launch Dev Container with [VSCode Dev Container Extension](https://code.visualstudio.com/docs/devcontainers/containers) or [GitHub Codespaces](https://github.com/features/codespaces).

### 2. Create .env file

Copy `.env.example` as `.env`

```
cp .env.example .env
```

1. Set `OPENAI_API_KEY` .
   You can find it in https://platform.openai.com/account/api-keys
2. Set `INPUT_FILE_PATH`, which is the path of the file to be summarized and `OUTPUT_FILE_PATH`, which is the path of the file to output the summary.

## Usage

### 1. Put the .tex file to be translated

Put the .tex file to be translated anywhere in the workspace.

.tex files exported from [Mathpix](https://mathpix.com/) are assumed as input.

### 2. Configure file paths

`TEX_PATH` (original .tex file put in 1.), `MD_PATH` (.md file with original content) and `TRANSLATION_MD_PATH` (translated .md file) are defined in top of [src/translate.ipynb](./src/translate.ipynb).
To change the file paths, edit the values of these variables.

To notice ChatGPT list of pair of original and translated sentences, `corr_list` should be set.

### 3. Run Jupyter Notebook Cells

Run all cells in [src/translate.ipynb](./src/translate.ipynb) sequentially.

## Example

See [/example](./example) directory.
