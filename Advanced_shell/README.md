## Project Overview & Summary

This project is a practical deep dive into Advanced Shell Scripting, focusing on automating interactions with a RESTful API (the Pokémon API). It progresses from simple, single API calls to complex operations involving parallel processing, robust error handling, and data summarization. The goal is to simulate real-world DevOps and Data Engineering tasks where automation, reliability, and efficiency are paramount.

#### **Learning Objectives**

By completing this project, you will learn and demonstrate proficiency in:

1.  **API Interaction:** Making HTTP requests from the command line using `curl`.
2.  **JSON Manipulation:** Parsing, filtering, and extracting data from JSON responses using `jq`.
3.  **Text Processing:** Utilizing the UNIX text processing trifecta (`grep`, `sed`, `awk`) to transform and format data.
4.  **Robust Scripting:** Implementing error handling, status checking, and retry logic to create reliable automation scripts.
5.  **Process Management:** Using shell job control (`&`, `wait`, `$!`) to run tasks in parallel, significantly improving script performance.
6.  **Data Reporting:** Aggregating data from multiple sources and generating structured reports (e.g., CSV files).
7.  **Modular Design:** Structuring scripts to be maintainable and adaptable for future changes.

#### **Key Concepts**

*   **HTTP Status Codes:** Checking `curl` exit codes or HTTP status codes (e.g., `200` OK vs. `404` Not Found) to determine the success or failure of a request.
*   **Idempotency and Retries:** Designing operations to be safely retried in case of transient network failures.
*   **Rate Limiting:** Understanding the constraints of external APIs and implementing delays to avoid being blocked.
*   **Concurrency vs. Parallelism:** Using background processes to achieve parallelism in a shell environment, understanding the associated challenges (e.g., shared resources, output interleaving).
*   **Data Pipelines:** Building a complete pipeline: data extraction (API) -> transformation (parsing) -> loading (saving to files) -> reporting (summary/analytics).

#### **Tools and Libraries**

*   **`curl`:** The primary tool for transferring data from or to a server. Used to make GET requests to the Pokémon API.
*   **`jq`:** A lightweight and powerful command-line JSON processor. Essential for parsing the API response and extracting specific fields.
*   **`awk`:** A versatile programming language for pattern scanning and processing. Used for text extraction, report generation, and calculating averages.
*   **`sed`:** A stream editor for filtering and transforming text. Used for specific text substitutions.
*   **Core Shell Utilities:** `grep`, `cut`, `echo`, variables, loops, conditionals, functions, and process control (`&&`, `||`).

#### **Real-World Use Case**

This project mirrors a common pattern in cloud and data engineering:

A **Data Engineer** needs to build a pipeline to collect data from various external SaaS platforms (e.g., Salesforce, Shopify, Twitter API) on a daily basis. 1. **Extraction:** The scripts from **Tasks 0, 2, 4, and 5** represent the data extraction layer. They must be robust, handle API failures gracefully, and efficiently pull data from all required endpoints. 2. **Transformation:** The scripts from **Tasks 1 and 3** represent the transformation layer. Raw JSON data is parsed, cleaned, and formatted into a more usable structure (like a CSV) for analysts. 3. **Loading:** The final JSON and CSV files are the loaded data, ready to be consumed by a database or a Business Intelligence (BI) tool like Tableau or Power BI.

The skills practiced here are directly applicable to building ETL (Extract, Transform, Load) or ELT pipelines using shell scripts, which is a lightweight and powerful approach for many tasks.
