🚀 Keploy C++ Unit Test Generator using LLM (Assignment 5)

This project implements a Unit Test Generator for C++ applications using a Large Language Model (LLM) like Ollama, following the workflow defined in Keploy's assignment. The tool takes a real-world C++ project (orgChartApi) and automatically generates, refines, and tests unit test cases with iterative feedback and build analysis.




📁 Project Structure

keploy-cpp-unit-test-generator/
├── CMakeLists.txt
├── tests/
│   └── sample_test.cpp
├── googletest/
│   └── (GoogleTest source files)
├── prompts/
│   ├── initial_prompt.yaml
│   ├── refine_prompt.yaml
│   └── fix_build_prompt.yaml
└── README.md




✅ Features

🧠 Utilizes LLMs to generate unit tests for C++ code

🔁 Refines test cases to remove duplicates and fix build errors

🔧 Automatically builds and checks coverage using CMake and GTest

🧪 Integrates with GNU coverage tools

📊 YAML-based structured prompts to guide the model

💡 Focused on real-world code (orgChartApi)





🛠 How It Works

1. Input: The C++ source files from the orgChartApi repo are given as input.


2. LLM Prompting:

An initial prompt with a YAML file is sent to the LLM to generate test files.



3. Test Generation:

The model creates C++ unit tests using the Google Test framework.



4. Refinement:

A second prompt improves test quality by removing duplicates and adding includes.



5. Build Process:

Tests are compiled using cmake and run.

On failure, build logs are sent to LLM to fix issues.



6. Coverage & Final Output:

If the build passes, test coverage is calculated.

Final cleaned-up test folder is ready for submission.



📦 Installation & Setup

1. Clone Repositories

git clone https://github.com/keploy/orgChartApi.git
git clone https://github.com/thiraviya2024/keploy-cpp-unit-test-generator.git

2. Install Prerequisites

CMake

g++

Python (optional for scripting)

Ollama (or your chosen LLM engine)

GoogleTest (included in googletest/ folder)


3. Build Tests

cd keploy-cpp-unit-test-generator
mkdir build
cd build
cmake ..
cmake --build .

4. Run Tests

ctest


📂 Prompts (YAMLs)

Prompts guide the LLM to:

Generate initial unit tests from source files.

Refine them with better structure and unique cases.

Handle compiler errors by auto-debugging.


📘 What I Learned

Running LLMs like Gemma using Ollama for developer workflows.

Generating and refining test cases with YAML prompt instructions.

Building end-to-end CI-compatible unit test automation for C++.

Using Google Test and CMake with LLM integration.


🔗 Useful Links

🔗 orgChartApi Repo

🔗 Ollama

🔗 Keploy


🙌 Acknowledgements

Thanks to the Keploy team and mentors for guiding us with the architecture and providing real-world problem statements. 💙
