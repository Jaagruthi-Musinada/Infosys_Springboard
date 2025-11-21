
## Web Application for Text Summarization, Paraphrasing, and Model Training

This project is a Streamlit-based web application that integrates secure authentication with transformer-based text processing features. The system includes user login, registration, OTP-based password reset, role-based dashboards, and tools for text summarization, paraphrasing, data augmentation, and model fine-tuning.

The application is designed to run inside Google Colab, where it is automatically deployed using ngrok to provide a public URL.

## Features

### 1. Authentication

* User registration and login
* Password hashing using bcrypt
* JWT-based session handling
* OTP-based password reset using SMTP
* Role-based access control (Admin and General User)

### 2. Admin Dashboard

* View all registered users
* Add new users
* Delete users (except the admin account)
* View usage analytics
* View complete usage logs and feedback submissions

### 3. User Dashboard

* Text summarization and paraphrasing tools
* Data augmentation utilities
* Light-weight model training and evaluation on T5-small
* BLEU, ROUGE-L, loss, and runtime evaluation
* Radar chart summarizing evaluation metrics
* Feedback submission module

### 4. Model Training and Evaluation

* Supports WikiAuto and CNN/DailyMail datasets
* Small samples used for fast, Colab-friendly demonstration
* Generates predictions and computes evaluation metrics
* Produces a radar chart to visualize performance

### 5. Deployment

* Fully automated deployment using Streamlit and ngrok
* Colab script writes the application file and launches it
* Previous Streamlit processes are automatically terminated


## How to Use

1. Open the Colab notebook containing the launcher script.
2. Insert your ngrok auth token and SMTP email credentials.
3. Run the full script.
4. A public ngrok link will be generated.
5. Open the link to access the application.

Admin default login:

* Email: `admin@ai`
* Password: `Infosys`



