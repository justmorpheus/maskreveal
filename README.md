# MaskReveal: Unmask Names from RC Details

**MaskReveal** is a script designed for educational Open-Source Intelligence (OSINT) purposes. It aims to unmask the name associated with RC (Registration Certificate) details using the car number plate of Indian drivers using Google's Gemini AI. The tool is strictly for learning and research purposes, **not for exploitation or illegal activities**.


---

## Features
- Resolves masked names from RC details by filling in placeholders (`*`).
- Utilizes Google's Gemini AI (`gemini-1.5-flash`) for predicting Indian name.

---

## Sources for Masked Names

You can obtain masked names from the following platforms by entering vehicle number plate (only for Indian vehicles):

1. **[CarInfo App](https://www.carinfo.app/)** - Provides masked RC details for vehicles.
2. **[VehicleInfo App](https://vehicleinfo.app/)** - A platform for vehicle information and RC details.
3. **[Vahan (Government of India)](https://vahan.parivahan.gov.in/)** - Official government platform requiring user registration.
4. **Other third-party websites** - Some platforms display masked names, such as `A*IS* A*MI*`.

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

3. **Configure the API Key**:
   - Replace `your_gemini_api_key_here` in the script with your actual Gemini API key.
   - You can obtain the API key from [Google Generative AI](https://cloud.google.com/genai/).

4. **Run the Tool**:
   ```bash
   python3 ai-guess.py "<masked-names-separated-by-comma>"
   ```
   **Example**:
   ```bash
   python3 ai-guess.py "R*AH*L K*UM*R, **AH*L K**MA*"
   ```
<img width="1600" alt="image" src="https://github.com/user-attachments/assets/a061c3c8-fdb1-4dc8-8ea0-b629c3830fae" />

5. **View Results**:
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
python3 ai-guess.py "R*AH*L K*UM*R, **AH*L K**MA*"
```

Output:
```
Resolved Name: R*AHHL KKUMMR*
Gemini-Suggested Name: Given the partially resolved name 'R*AHHL KKUMMR*', and knowing it's an Indian name, a likely solution is:

**RAHUL KUMAR**
```

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


## Credits:
- Chatgpt
- Gemini AI
- https://start.me/p/vjR5wL/osint-india
