# API Fuzzer

## Overview

API Fuzzer is a fast and efficient tool designed for testing APIs by sending thousands of requests based on a specified JSON configuration. With its customizable request format, you can easily adjust methods, URLs, and payload data to perform extensive fuzz testing.

## Features

- **High Performance**: Capable of handling thousands of requests quickly.
- **Customizable Requests**: Easily modify request methods, URLs, and data.
- **Token Handling**: Supports API token authentication by allowing you to modify headers.

## Installation

1. Ensure you have Python installed on your machine (Python 3.x recommended).
2. Clone the repository or download the `Fuzzer.py` script.

   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```
## Usage

1. Create a `request.json` file to define your API requests. The format should be as follows:

   ```json
   [
       {"METHOD": "GET", "URL": "https://api.example.com/endpoint", "DATA": ""},
       {"METHOD": "POST", "URL": "https://api.example.com/endpoint", "DATA": "{\"key\":\"value\"}"}
   ]
   ```

   Each request should be defined as a JSON object within the array. Modify `METHOD`, `URL`, and `DATA` as needed.

2. Open the `Fuzzer.py` file and update the necessary header parameters, including the API token if required.

3. Run the fuzzer with the following command:

   ```bash
   python Fuzzer.py --headers '{"key":"value"}' -w <wordlist-path>
   ```

   Replace `<wordlist-path>` with the path to your wordlist file if needed. 

## Example

Here’s an example of what your `request.json` might look like:

```json
[
    {"METHOD": "GET", "URL": "https://api.example.com/user", "DATA": ""},
    {"METHOD": "POST", "URL": "https://api.example.com/user", "DATA": "{\"name\":\"test\"}"}
]
```

## Contributing

If you would like to contribute to the project, please fork the repository and submit a pull request with your changes. Ensure you include tests for any new features or bug fixes.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

## Support

For any issues or questions, feel free to open an issue in the repository or contact the author directly.

---

Happy fuzzing! 🚀
