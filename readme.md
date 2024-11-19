# Web Server with Testing Functionality

---

## Overview

This project implements a **static web server** in Go, capable of serving files dynamically while managing errors and MIME types efficiently. The project also includes comprehensive tests to ensure robust functionality.

---

## Code Structure

### `main.go`
- **Implements the web server**.
- Serves static files from the `templates/` directory.
- Handles missing files with `404 Not Found`.

### `main_test.go`
- Uses Go’s `httptest` package to:
  - Simulate HTTP requests.
  - Validate server behavior under various scenarios.

---

## Key Features

1. **Dynamic File Serving**:
   - Automatically serves static files based on client requests.

2. **Error Handling**:
   - Responds with appropriate `404 Not Found` for missing files.

3. **MIME Type Management**:
   - Ensures files are served with correct MIME types, such as `text/html` or `text/css`.

---

## Best Practices

### Dependency Management
- Initialize Go modules for dependency management:
  ```bash
  go mod init github.com/Krishna868601/webserver
  ```
  
---

## Testing Recommendations

### Comprehensive Tests
- Ensure tests cover edge cases, including:
  - **Missing Files**
  - **MIME Type Mismatches**

### Check Test Coverage
- Use the following command to verify test:
  ```bash
  go test -v
  ```
  ![image](https://github.com/user-attachments/assets/3f3d6646-3970-4edc-89f7-739b04d2bfc3)

# Examples

---

## Accessing a File
1. Open your browser.
2. Navigate to the following URL:
   ```bash
   http://localhost:80/index.html
   ```

## Handling a Missing File

1. Open your browser.
2. Navigate to the following URL:
   ```bash
   http://localhost:80/missing.html
   ```
## Challenges and Solutions

### Challenge 1: MIME Type Mismatch
- **Problem**: Modern browsers expect `text/javascript` for JavaScript files.
- **Solution**: Update tests to recognize modern MIME types like `text/javascript`.

### Challenge 2: Handling Missing Files
- **Problem**: Missing files can disrupt server behavior, causing unhandled errors.
- **Solution**: Use Go’s `http.FileServer` to handle `404 Not Found` errors gracefully and provide a consistent response.

### Challenge 3: Ensuring Test Coverage
- **Problem**: Validating all edge cases in a server can be difficult.
- **Solution**: Simulate diverse HTTP requests and scenarios using Go’s `httptest` package to ensure comprehensive test coverage.

## How to Run

### Start the Server
Run the following command to start the server:

```bash
go run main.go
```
## Run Tests

Execute tests with the following command:

```bash
go test -v

   
   
   

  

  

  
