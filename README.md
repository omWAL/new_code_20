# Run C++ Code on Windows

## Step 1: Install Compiler

Install MinGW or [Code::Blocks](https://www.codeblocks.org?utm_source=chatgpt.com)

Recommended:

* Install Code::Blocks with MinGW compiler

---

## Step 2: Create C++ File

Create file:

```text
main.cpp
```

Example code:

```cpp
#include <iostream>
using namespace std;

int main()
{
    cout << "Hello";
    return 0;
}
```

---

## Step 3: Open Terminal

Open:

* Command Prompt
  OR
* PowerShell

---

## Step 4: Go to File Location

Use `cd` command:

```bash
cd Desktop
```

Example:

```bash
cd Desktop/cpp
```

---

## Step 5: Compile Code

```bash
g++ main.cpp -o main
```

Explanation:

* `g++` → compiler
* `main.cpp` → source file
* `-o main` → output file name

---

## Step 6: Run Program

```bash
main
```

OR

```bash
.\main
```

Output:

```text
Hello
```

---

# Run C++ Code on Linux

## Step 1: Install g++

For Ubuntu/Debian:

```bash
sudo apt update
sudo apt install g++
```

For Fedora:

```bash
sudo dnf install gcc-c++
```

---

## Step 2: Create File

```bash
nano main.cpp
```

Paste code:

```cpp
#include <iostream>
using namespace std;

int main()
{
    cout << "Hello";
    return 0;
}
```

Save:

* CTRL + O
* ENTER
* CTRL + X

---

## Step 3: Compile Program

```bash
g++ main.cpp -o main
```

---

## Step 4: Run Program

```bash
./main
```

Output:

```text
Hello
```

---

# One Command Method (Linux)

Compile and run together:

```bash
g++ main.cpp -o main && ./main
```

---

# Check Compiler Version

Windows/Linux:

```bash
g++ --version
```

---

# Common Errors

## Error:

```text
'g++' is not recognized
```

Reason:

* Compiler not installed
* PATH not set

---

## Error:

```text
Permission denied
```

Linux fix:

```bash
chmod +x main
```

---

# Simple Workflow

## Windows

```text
Write Code → Compile → Run
```

Commands:

```bash
g++ file.cpp -o file
.\file
```

---

## Linux

Commands:

```bash
g++ file.cpp -o file
./file
```
