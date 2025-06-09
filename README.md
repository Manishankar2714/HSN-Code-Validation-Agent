# HSN-Code-Validation-Agent
# 📦 HSN Code Validation & Suggestion Agent (Using Google ADK)

This project is an **Intelligent Agent** built using the **ADK (Agent Developer Kit)** by Google. It is designed to **validate HSN codes** and **suggest appropriate HSN codes** based on user input descriptions of goods or services.

---

## 🧠 Objective

- ✅ Validate HSN codes against a master dataset.
- 💡 Suggest appropriate HSN codes based on textual descriptions.
- 🧰 Built using the **Google ADK Framework**.

---

## 📁 Dataset

The agent uses a master Excel file with the following structure:

| HSNCode | Description                      |
|---------|----------------------------------|
| 0101    | LIVE HORSES, ASSES, MULES...     |
| 010110  | PUREBRED BREEDING ANIMALS...     |
| ...     | ...                              |

📥 Download the dataset here:  
[HSN_Master_Data.xlsx](https://docs.google.com/spreadsheets/d/1UD4JAAQ6Fgeyc5a1OwBiLV2cPTAK_D2q/edit?usp=sharing)

---

## 🏗️ Agent Architecture

### Components:

- **Intent Handler**: Detects whether the user wants to validate or get a suggestion.
- **Validation Engine**:
  - Format validation (2–8 digits, numeric)
  - Existence check
  - Hierarchical validation
- **Suggestion Engine**:
  - Uses fuzzy string matching to suggest relevant HSN codes based on description
- **Data Loader**:
  - Loads `HSN_Master_Data.xlsx` using `pandas` for efficient access
- **Response Generator**:
  - Returns success/failure messages and suggestions to the user

---

## 🚀 Features

- 🔍 **HSN Code Validation**  
  Checks if the code exists and is valid according to format and dataset.

- 💡 **HSN Code Suggestion**  
  Suggests one or more HSN codes that best match the given goods/service description.

- 🔄 **Hierarchical Check**  
  For full-length codes (e.g., `01011010`), checks for parent codes (`010110`, `0101`, etc.).

---

## 🖥️ Technologies Used

- `Python 3`
- `pandas`
- `fuzzywuzzy` / `difflib` for fuzzy matching
- `ADK` (Agent Developer Kit by Google)
- `openpyxl` for reading Excel files

---


