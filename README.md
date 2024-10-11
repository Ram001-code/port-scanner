# Port Scanner with Flask and Nmap

## 📖 Overview

The **Port Scanner** is a web-based tool that leverages **Nmap**, a powerful network scanning utility, to perform port scans on any given domain or IP address. Built with **Flask** and designed with a clean, user-friendly interface, this tool makes it easy to explore network services and open ports. Whether you're a network administrator or a security enthusiast, this tool simplifies port scanning for your needs.

---

## 🌐 Working WEB-APP

You can view my **Port Scanner** Project Live at this [here](https://ports.ramksites.site/).

---

## 📂 Project Structure

```
port_scanner/
├── Dockerfile              # Dockerfile to containerize the application
├── app.py                  # Flask application for handling requests and executing Nmap scans
├── requirements.txt        # Python dependencies
├── static/
│   └── styles.css          # CSS for the front-end design
└── templates/
    └── index.html          # Front-end HTML for the web application
```

---

## 🚀 Features

1. **Web-Based Interface**:
   - Input a domain or IP address to scan.
   - Optionally provide custom Nmap flags for advanced scans.
2. **Nmap Integration**:
   - Executes Nmap commands directly from the Flask backend.
   - Displays real-time scan results in the browser.
3. **Lightweight and Responsive Design**:
   - Built with minimal CSS for a sleek and modern interface.
4. **Containerized**:
   - Easily deployable using Docker.

---

## 🛠️ Technologies Used

- **Backend**: Flask (Python)
- **Frontend**: HTML, CSS, JavaScript
- **Port Scanning**: Nmap
- **Containerization**: Docker

---

## ⚙️ Prerequisites

Before running this project, ensure you have the following installed:

- **Python 3.9 or higher**
- **Docker** (if you want to containerize the app)
- **Nmap** (if running locally, it’s already included in the Docker image)

---

## 🖥️ Setup Instructions

### Local Setup

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Ram001-code/port_scanner.git
   cd port_scanner
   ```

2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Application**:
   ```bash
   python app.py
   ```

4. **Access the Application**:
   Open your browser and visit:
   ```
   http://127.0.0.1:5000
   ```

### Docker Setup

1. **Build the Docker Image**:
   ```bash
   docker build -t port_scanner .
   ```

2. **Run the Container**:
   ```bash
   docker run -d -p 5000:5000 --name port-scanner-container port_scanner
   ```

3. **Access the Application**:
   Open your browser and visit:
   ```
   http://<your-ip>:5000
   ```

---

## 🧰 Usage

1. **Enter the Target**: Input a domain or IP address in the provided field.
2. **Customize with Flags (Optional)**:
   - Example: `-sS -p 1-1000` for a stealth scan on the top 1000 ports.
3. **Run the Scan**: Click "Scan" to initiate the process.
4. **View Results**: The scan progress and results will appear in the output section.

---

## 📦 Docker Details

- **Port Mapping**: The application listens on port `5000` inside the container. You can map it to any port on your host.
- **Command to Run**:
   ```bash
   docker run -d -p 6666:5000 port_scanner
   ```
- **Access the Application**:
   ```
   http://<host-ip>:6666
   ```


## 📄 Example Output

1. **Scan Summary**:
   - Target: `example.com`
   - Open Ports: `22, 80, 443`
   - Scan Duration: `26 seconds`

2. **Detailed Results**:
   - **Port 22**: SSH (OpenSSH 9.2p1)
   - **Port 80**: HTTP (nginx 1.22.1)
   - **Port 443**: HTTPS (nginx 1.22.1)

---

## 🛡️ Security Considerations

- Only use this tool for domains and IPs you are authorized to scan.
- Misuse of Nmap for unauthorized scans is illegal and against ethical guidelines.

---

## 🤝 Contribution

Contributions are welcome! If you’d like to add features, fix bugs, or improve documentation:

1. Fork the repository.
2. Create a new branch for your feature:
   ```bash
   git checkout -b feature-name
   ```
3. Submit a pull request.

---

## 📧 Contact

For any inquiries or support, reach out to:

- **Author**: Ram Kansal
- **Email**: ramkansal9822@gmail.com
- **GitHub**: [Ram001-code](https://github.com/Ram001-code)

---

## 🌟 Acknowledgments

Special thanks to the creators of **Nmap** and the **Flask** framework for providing the tools to build this project.