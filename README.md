# Digital Banking Fraud Detection & Simulation Engine

## Project Overview

This project is a secure digital banking backend system that detects fraudulent transactions using a Hybrid Fraud Detection Model (Rule-Based + Machine Learning).

It is built using:
- Spring Boot
- MySQL
- JWT Authentication
- Random Forest (Flask ML Service)

---

## How It Works

1. User provides:
   - Sender account number
   - Receiver account number
   - Amount
   - PIN

2. Backend performs:
   - PIN validation using BCrypt
   - Balance verification
   - Automatic fraud feature generation
   - Rule-based fraud checks
   - Machine Learning fraud prediction
   - Hybrid score calculation

3. Final Decision:
   - HIGH_RISK → BLOCKED
   - MEDIUM_RISK → REVIEW_PENDING
   - SAFE → SUCCESS

---

## Fraud Detection Logic

Rule-Based:
- High amount (≥ 50,000)
- Blacklisted receiver
- Rapid transactions

Machine Learning:
- Algorithm: Random Forest
- Predicts fraud probability
- Risk thresholds:
  - ≥ 0.7 → High Risk
  - ≥ 0.4 → Medium Risk

Final Score = Rule Score + (ML Probability × 100)

---

## Security Features

- JWT Authentication
- Role-based access (ADMIN / USER)
- BCrypt PIN encryption
- Environment variable based DB credentials

---

## Technologies Used

- Java 17
- Spring Boot 3
- MySQL
- Flask
- Random Forest (Scikit-learn)

---

## Conclusion

This project simulates a real-world digital banking fraud detection system using secure backend development and hybrid machine learning integration.
