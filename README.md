# ML Model Deployment on AWS EC2

This guide outlines the steps to deploy a machine learning model on an AWS EC2 instance using Flask.

## Create the ML Model

* Export your trained model into a `.pkl` file using pickle.

## Deployment Steps

1. **Create an AWS Account:** If you don't have one, sign up at [https://aws.amazon.com/](https://aws.amazon.com/).

2. **Create an EC2 Instance:**
   * Log in to the AWS Management Console.
   * Navigate to the EC2 service.
   * Click on "Launch Instance."
   * Choose an Amazon Machine Image (AMI) with your desired operating system.
   * Select an instance type.
   * Configure instance details.
   * Create or select an existing key pair.
   * Launch the instance.

3. **Configure Security Group:**
   * Open the EC2 instance details.
   * Go to the "Security" tab.
   * Click on the security group.
   * Add an inbound rule to allow traffic on port 8080 (or your desired port).

4. **Download PuTTY and WinSCP:**
   * Download and install from their official websites.

5. **Use WinSCP to Transfer Files:**
   * Open WinSCP.
   * Enter the hostname (public IP or DNS name) of your EC2 instance.
   * Enter the username and select the private key file (`.ppk`).
   * Click "Login."
   * Transfer `model.pkl`, `app.py`, and `requirements.txt` to the EC2 instance.

6. **Access the EC2 Server using PuTTY:**
   * Open PuTTY.
   * Enter the hostname of your EC2 instance.
   * Enter the username and select the private key file.
   * Click "Open."

7. **Install Dependencies:**
   * Install Python3: 
     ```bash
     sudo apt update && sudo apt install python3-pip
     ```
   * Install project dependencies: 
     ```bash
     pip install -r requirements.txt
     ```

8. **Run the Flask App:**
   ```bash
   python3 app.py

9. **Access the Application:**
   * Open your web browser.
   * Enter http://<EC2 public IPv4 address>:8080
   * Note: Replace placeholders like <EC2 public IPv4 address> with actual values.
