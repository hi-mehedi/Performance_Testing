# Performance Testing with Apache JMeter

## Overview
This project is designed to conduct comprehensive performance testing using **Apache JMeter**. It includes a **.jmx** test plan that enables users to simulate multiple user loads, analyze system behavior, and generate insightful performance reports. By leveraging JMeter's capabilities, users can evaluate the scalability and reliability of applications under various conditions.

## Features
- **Load Testing**: Simulate concurrent users to analyze application performance.
- **Automated Test Execution**: Execute tests seamlessly using the command-line interface.
- **Detailed Reports**: Generate informative **HTML performance reports** for result analysis.
- **Structured Project Setup**: Well-organized directory structure for easy test execution and maintenance.

## Technologies Used
- **Apache JMeter** - A powerful open-source performance testing tool.
- **Java** - Required runtime environment to execute JMeter.
- **Command-line Interface (CLI)** - Used for executing test scripts and generating reports.

## How to Install and Set Up JMeter
To successfully run this project, you need to install JMeter and configure it properly.

1. **Download JMeter**:
   - Visit the official Apache JMeter website: [JMeter Download Page](https://jmeter.apache.org/download_jmeter.cgi)
   - Download the latest **binary** version (ZIP or TGZ format) for your operating system.
   - Extract the downloaded file to your desired location.

2. **Ensure Java is Installed**:
   - JMeter requires **Java 8 or higher**.
   - Check if Java is installed by running:
     ```sh
     java -version
     ```
   - If Java is not installed, download and install it from [Oracle Java Downloads](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) or use OpenJDK.

3. **Set Up JMeter**:
   - Navigate to the extracted JMeter folder.
   - Inside the folder, locate the `bin` directory where JMeter executables reside.

## How to Clone and Set Up the Project
To use this project effectively, follow these steps:

1. **Clone the Repository**:
   ```sh
   git clone <repository-url>
   ```
2. **Move to JMeter's `bin` Directory**:
   ```sh
   cd <path-to-jmeter>/bin
   ```
3. **Place the `per_-t500.jmx` File**:
   - Copy the provided **`per_-t500.jmx`** file into the `bin` folder.
   - This step is crucial as JMeter needs the test plan to be inside its `bin` directory for execution.
4. **Manually Create a `report` Folder**:
   - Inside the `bin` directory, create a folder named `report` to store test results.
   ```sh
   mkdir report
   ```

## How to Open `per_-t500.jmx` in JMeter GUI
To inspect or modify the test plan, follow these steps:

1. **Launch JMeter**:
   - Navigate to the `bin` directory and execute:
     ```sh
     jmeter
     ```
   - This opens the JMeter GUI.

2. **Load the Test Plan**:
   - Click on `File` > `Open`.
   - Select `per_-t500.jmx` from the `bin` folder.
   - The test plan will be displayed in the JMeter interface, allowing modifications and manual execution.

## Running the Performance Test
To execute the performance test using JMeter in **non-GUI mode**, run the following command inside the `bin` folder:
```sh
jmeter -n -t per_-t500.jmx -l report/per_-t500.jtl
```
This command:
- Runs JMeter in **non-GUI mode** (`-n`) to optimize resource usage.
- Loads the test plan file (`-t per_-t500.jmx`).
- Saves the test results in **JTL format** (`-l report/per_-t500.jtl`).
- Requires the `report` folder to exist before running the test.

## Generating the Performance Report
After executing the test, generate a detailed **HTML performance report** by running:
```sh
jmeter -g report/per_-t500.jtl -o report/per_-t500.html
```
This command:
- Takes the raw test result file (`.jtl`).
- Generates a structured **HTML report** inside the `report` folder for in-depth analysis.
- Requires the `report` folder to be created manually before running the test.

## Understanding the `per_-t500.jmx` Test Plan
The provided **`per_-t500.jmx`** file is a pre-configured JMeter test plan that includes:
- **Thread Groups**: Defines the number of users, ramp-up period, and loop count.
- **Samplers**: Requests to be sent to the target application.
- **Listeners**: Components used to collect and analyze test results.
- **Assertions**: Conditions to verify application responses.

## Notes
- **Ensure Java is installed and configured properly before running JMeter.**
- **Place the .jmx file inside the `bin` folder for smooth execution.**
- **Manually create the `report` folder inside the `bin` directory before running test commands.**
- **Running tests in non-GUI mode is recommended for better performance.**

## Report
![image](https://github.com/user-attachments/assets/6d04c8cd-0898-4ece-ada1-40e35c09b61e)
![image](https://github.com/user-attachments/assets/24e0757c-71b9-42c7-9cee-f85a605dbb5b)

## Author
**Mehedi Hasan Soumik**



