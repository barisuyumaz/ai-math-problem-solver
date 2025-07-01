# 🧠 Math Solver AI Demo

This is a **demo project** that uses OpenAI's GPT API to solve math problems from images with step-by-step explanations. Originally developed for a case task, it's now shared as a public technical demo.

## 🚀 Features

- 📷 Extracts math problems from images using OCR (Tesseract)
- 🧠 Automatically detects the topic of the math problem (e.g. algebra)
- 🤖 Solves the problem step-by-step using GPT-4o or Symbolab when needed
- 💬 Outputs are structured and explained in a friendly, teacher-like tone
- 🔁 Consistent results thanks to `temperature = 0` setting

## 🧪 Technologies Used

- Python 3.11
- OpenAI GPT-4o API
- Tesseract OCR (via pytesseract)
- PIL (Image handling)
- Selenium + BeautifulSoup (for Symbolab integration)

## 📸 Example

**Input Image Content:**

```
2x - 3 = -7
```

**Output Response:**

```
Problem is: 2x−3=−7  
1. Move 3 to the right side:  
2x = -4  
2. Divide both sides by 2:  
Result is: x = -2
```

## 💡 Prompt Design (GPT API)

```text
The math problem in the image is related to {math_topic}.
Analyze the problem as if you are a mathematics teacher specializing in {math_topic}.
Your task is to solve the problem in a clear, step-by-step manner with accuracy
and a friendly tone like starting the sentence with "Lets" in step-by-step section.
```

This structure ensures consistent and accurate results, optimized for cost-efficiency and clarity.

## 📝 Notes

- The topic detection is done via simple regex-based classification.
- For algebraic equations, the app scrapes Symbolab to fetch detailed solution steps.
- GPT is only used when problems are complex or require structured explanation.
- Image must be under 20MB (API input limit).

## ⚠️ Disclaimer

This project is a **personal demo**, not a commercial product. It was originally built as a proof-of-concept for a job application case.

## 📄 License

This project is not open source. Shared for demonstration and portfolio purposes only.
