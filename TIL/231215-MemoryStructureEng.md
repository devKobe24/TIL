# Memory Structure 🧩

When a program is executed, the **operating system (OS) allocates memory (RAM) space for that program.** This space is divided into the following four components:

1. **Code**
2. **Data**
3. **Heap**
4. **Stack**

The diagram below illustrates the memory and its components:

![Memory Structure](https://github.com/devKobe24/images/blob/main/memory-struct.png?raw=true)

## 1️⃣ Code Section

The **"source code"** written by developers is stored in machine-readable form. This is determined at **"compile time"** and is stored as **"Read-Only"** to prevent code from being modified during execution.

## 2️⃣ Data Section

This section stores **global variables** and **static** variables. Memory is allocated for them when the program starts, and the memory is released when the program terminates. The variables in this section can be modified during execution, so they are designated as **"Read-Write."**

## 3️⃣ Heap Section

The **"memory area allocated and deallocated by the programmer"** is called the heap. Programmers can allocate memory on the heap using functions like **"malloc"** and **"calloc,"** which is known as **"dynamic allocation."** It's essential to free the allocated memory when it's no longer needed; otherwise, it can lead to **"memory leaks."**

Unlike Code, Data, and Stack, Heap's size is not determined at compile time, making it suitable for cases where the data size is uncertain.

### 3.1 Pros and Cons of the Heap

**Pros:**
- No size limit for memory allocation.
- Essentially global in scope, accessible from all functions in the program.

**Cons:**
- Slower due to allocation and deallocation operations.
- Risk of heap corruption (double freeing, using after free, etc.).
- Possibility of heap contention (when multiple threads attempt to access simultaneously).
- Requires manual memory management (failure to free memory can result in memory leaks).

## 4️⃣ Stack Section

The stack section stores **local variables, function parameters, return values,** and other function-related data. Memory allocated for these items is automatically released when the function exits. The size of this section is determined at **"compile time,"** and there is a limit to the amount of memory that can be allocated.

### 4.1 Pros and Cons of the Stack

**Pros:**
- Very fast due to efficient CPU management of stack memory.
- No need to manually free memory.

**Cons:**
- Limited memory size.
- Limited to accessing local variables.

### 🍗 Digging into the Sentences (1) !!

1️⃣ Source Code (Source code)

🙋‍♂️ **"Source code is a human-readable text-based code used to write computer programs."** This code is written using a programming language but exists in a form that can be understood and modified by humans before it is translated into machine code that computers can understand.

Source code includes commands, functions, variables, and other elements used in program development and plays a crucial role in defining the program's behavior.
Source code is typically written using text editors or integrated development environments (IDEs).

2️⃣ Machine Language (Machine language)

🙋‍♂️ **"Machine language is the lowest-level programming language that a computer can directly understand and execute."** It is represented as binary code that the computer's central processing unit (CPU) can understand, consisting of patterns of 0s and 1s. Each bit pattern represents a computer instruction or data.

Machine language is architecture-specific, and each CPU or processor has its unique machine language that it can understand.
Therefore, to run on different computer architectures, programs must be written in the appropriate machine language.

Machine language is challenging for humans to understand and write, and programming directly in machine language is complex and error-prone.
As a result, most programmers use high-level programming languages (e.g., C, C++, Java, Swift, etc.) to write programs, and these high-level languages are translated into machine code through compilation or interpretation.

In summary, machine language is binary code that computers directly execute, architecture-specific, and challenging for humans to understand and write.
Programs written in high-level languages are typically translated into machine code for execution.

3️⃣ Compile Time (Compile Time)
**"Compile time refers to the time when a program is compiled, which is the process of translating source code into machine code or intermediate code using a compiler."**

Compile time is an important phase in program development, where tasks such as compiling source code, detecting errors, and optimizing code are performed.
Addressing issues and errors that occur during compile time can improve the program's stability and performance.

### 🍗 Digging into the Sentences (2) !!

1️⃣ Static

The **"static"** keyword is used within classes or structures to indicate that a particular member (variable or method) belongs to the type itself and is not associated with instances. It is also referred to as a **"type method"** or **"type property."**

Members defined with the **"static"** keyword are shared among all instances of the class or structure because they belong to the class or structure type itself.

These members can be accessed directly on the class or structure type, unlike instance properties or methods.
The **"static"** keyword is often used to create utility methods or properties that are not tied to specific instances but are related to the overall type.
