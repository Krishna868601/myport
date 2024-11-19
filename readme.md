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
- Use the following command to verify test coverage:
  ```bash
  go test -cover
  ```
  

  
