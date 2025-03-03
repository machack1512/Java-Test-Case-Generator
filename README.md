# 🚀 **Java Test Case Generator**

The **Java Test Case Generator** is a powerful VSCode extension designed to automate the creation of random test cases for Java functions. By defining custom constraints, developers can easily generate diverse test cases, including edge cases, ensuring comprehensive code coverage. This extension is seamlessly integrated with VSCode, providing a smooth and efficient user experience.

---

## 🛠 Tech Stack

- **Frontend:** VSCode API, TypeScript
- **Backend:** Node.js
- **Testing:** Mocha, Chai
- **Deployment:** VSCode Marketplace

---

## 📁 **Project Structure**

```
/java-testcase-generator
├── backend-java/          # Spring Boot Backend
│   ├── src/main/java/
│   │   ├── controller/
│   │   ├── service/
│   │   ├── model/
│   │   ├── repository/
│   │   ├── config/
│   ├── pom.xml
│
├── backend-node/          # Node.js API for Test Case Logic
│   ├── src/
│   │   ├── routes/
│   │   ├── controllers/
│   │   ├── models/
│   ├── package.json
│
├── frontend/              # Vue.js Dashboard
│   ├── src/
│   │   ├── components/
│   │   ├── views/
│   │   ├── router/
│   ├── package.json
│
├── database/              # MongoDB schema
│
├── deployment/            # Docker and Kubernetes configurations
│   ├── Dockerfile
│   ├── docker-compose.yml
│   ├── k8s-deployment.yaml
│
└── README.md
```

---

## ⚡ Features

- **Random Test Case Generation:** Automatically generates random test cases based on user-defined constraints for Java functions.
- **Input Constraints:** Define custom ranges or specific allowed values for input variables.
- **Multiple Test Cases:** Generate multiple test cases at once for faster testing.
- **Edge Case Testing:** Ensure your Java functions are thoroughly tested with a variety of edge cases.
- **VSCode Integration:** Built directly into the VSCode environment for a smooth and intuitive user experience.

---

## 📦 Installation

### Prerequisites

Before you begin, ensure the following are installed on your machine:

- **Visual Studio Code** – The code editor where the extension will be used.
- **Node.js** – Required for building and packaging the extension.
- **VSCode Extension API** – For developing extensions within the VSCode environment.

### Setup Instructions

1. **Clone the repository** to your local machine:

    ```bash
    git clone https://github.com/your-username/java-test-case-generator.git
    cd java-test-case-generator
    ```

2. **Install dependencies**:

    ```bash
    npm install
    ```

3. **Compile and package** the extension:

    ```bash
    npm run package
    ```

4. **Install the extension** in your local VSCode instance:

    - You can install it manually using the `.vsix` file generated by the `npm run package` command.
    - Alternatively, publish it to the **VSCode Marketplace** for wider usage.

---

## 🏗 Usage

Once installed, follow these steps to start generating test cases:

1. **Open your Java file** in VSCode where you'd like to generate test cases.
2. **Define Input Constraints**:
    - Specify the range or set of allowed values for each input variable.
3. **Run the Test Case Generator**:
    - Open the **Command Palette** (`Ctrl+Shift+P`), search for `Java Test Case Generator`, and select the command to generate test cases.
4. **View Generated Test Cases**:
    - The generated test cases will be displayed in the **VSCode Output Panel**, ready for easy copying and pasting into your test files.

---

## 📝 Example

### Java Function:

```java
public class Calculator {
    public int add(int a, int b) {
        return a + b;
    }
}
```

### Input Constraints:

- `a` in range 1–10
- `b` in range 1–5

### Generated Test Cases:

```java
add(1, 1)
add(2, 4)
add(3, 5)
add(10, 1)
```

These test cases will be displayed in the Output Panel for easy integration into your test files.

---

## ⚙ Example Configuration

Define your input constraints in the settings as shown below:

```json
{
    "javaTestCaseGenerator.variables": [
        {
            "name": "a",
            "type": "int",
            "range": [1, 10]
        },
        {
            "name": "b",
            "type": "int",
            "range": [1, 5]
        }
    ]
}
```

---

## 🛠 Troubleshooting

- If you encounter issues, check the **VSCode Output Panel** for error messages.
- Ensure that input constraints are correctly defined in the settings.
- Verify that your Java code is well-formed and free from errors.

---


## 🐛 Bug Reports & Feature Requests

If you find a bug or have a feature request, please open an issue in the repository. Provide as much detail as possible, including any error messages or logs.

---

## 📝 License

This project is licensed under the **MIT License**. See the [LICENSE](./LICENSE) file for more details.

---
