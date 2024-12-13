# MaskReveal: Unmask Names from RC Details

**MaskReveal** is a script designed for educational Open-Source Intelligence (OSINT) purposes. It aims to unmask names associated with RC (Registration Certificate) details derived from car number plates of Indian drivers using Google's Gemini AI. The tool is strictly for learning and research purposes, **not for exploitation or illegal activities**.

---

## Features

- Resolves masked names from RC details by filling in placeholders (`*`).
- Utilizes Google's Gemini AI (`gemini-1.5-flash`) for predicting Indian names.
- Supports both direct API key input and environment variable configuration for seamless usage.

---

## Sources for Masked Names

You can obtain masked names from the following platforms by entering vehicle number plate details (specific to Indian vehicles):

1. **[CarInfo App](https://www.carinfo.app/)** - Provides masked RC details for vehicles.
2. **[VehicleInfo App](https://vehicleinfo.app/)** - A platform for vehicle information and RC details.
3. **[Vahan (Government of India)](https://vahan.parivahan.gov.in/)** - Official government platform requiring user registration.
4. **Other third-party websites** - Some platforms display masked names, such as `R*AH*L K*UM*R`.

> **Note**: This tool focuses on unmasking names obtained from non-government sources where masked details are publicly available. It is not exploiting any vulnerability or misconfiguration.

---

## Installation and Setup

### Prerequisites

- Python 3.8 or later.
- A valid Google Generative AI API Key.

### Steps to Install and Run

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/justmorpheus/maskreveal
   cd maskreveal
   ```

2. **Install Dependencies**:
   ```bash
   pip install google-generativeai
   ```

3. **Run the Tool**:
   
   #### Option 1: Passing the API Key Directly
   ```bash
   python3 maskreveal_script.py "<masked-names-separated-by-comma>" --ai-key "<your_gemini_api_key_here>"
   ```

   #### Option 2: Using an Environment Variable for the API Key
   ```bash
   export AI_KEY="<your_gemini_api_key_here>"
   python3 maskreveal_script.py "<masked-names-separated-by-comma>"
   ```

   **Example**:
   ```bash
   python3 maskreveal_script.py "R*AH*L K*UM*R, **AH*L K**MA*" --ai-key AIzaSyBsZvD7OWAor5PkE0G0yZMk4t4NWhrQy4s
   ```

4. **View Results**:
   - The tool outputs the resolved name and Gemini AI's suggested full name.

---

## How It Works

1. The tool accepts a comma-separated string of masked names.
2. It resolves the name by:
   - Comparing character positions across multiple inputs.
   - Filling placeholders (`*`) with the most probable letters.
3. The resolved name is passed to Gemini AI for prediction, which suggests the most likely full name.

---

## Example Output

Input:
```bash
python3 maskreveal_script.py "R*AH*L K*UM*R, **AH*L K**MA*"
```

Output:
```
Resolved Name: R*AHHL KKUMMR*
Gemini-Suggested Name: The most likely full name is **RAHUL KUMAR**.
```

<img width="1727" alt="image" src="https://github.com/user-attachments/assets/6a4d6d74-c601-43d2-bd1a-54207fdd6a6d" />

---

## Disclaimer

- **For Educational Use Only**: This tool is intended for learning and research purposes.
- **User Responsibility**: Users are responsible for ensuring ethical and legal use of this tool.
- **No Corporate Endorsement**: This tool is not endorsed by any company or employer.
- **Respect Privacy**: Do not use this tool to invade someone's privacy or for malicious purposes.

---

## Suggested Use Cases

- **Learning OSINT Techniques**: Understand how masked data can be analyzed and completed.
- **Educational Demonstrations**: Showcase AI's capabilities in predictive analytics.

> **Important**: Always comply with local laws and platform terms when using this tool.

---

## Credits:

- **ChatGPT** - Natural Language Processing.
- **Gemini AI** - Name prediction and content generation.
- **OSINT Community: https://start.me/p/vjR5wL/osint-india**
---

For additional help or feedback, please open an issue on the repository.

