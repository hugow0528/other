Here is the OCR transcript of the worksheet followed by the completed exercises with explanations in both Cantonese and English.

---

### Part 1: OCR of the Worksheet

**Page 1**
*   **Title:** Worksheet: Tracing the Machine Cycle
*   **Topic:** Fetch-Decode-Execute Cycle
*   **Program:** Adding Two Inputs
*   **Program Listing:**
    *   00: INP (Input a number)
    *   01: STA num1 (Store it in memory (num1))
    *   02: INP (Input another number)
    *   03: ADD num1 (Add value stored in num1)
    *   04: OUT (Output the result)
    *   05: HLT (Stop the program)
    *   06: num1 DAT 00 (Memory location for first number)
*   **Sample Trace for Instruction 00 (INP):**
    *   Fetching: Set MAR to 0; Increment PC to 1; Fetch instruction from MAR; Fetched instruction: 901 stored in MDR; Copy to CIR.
    *   Decoding: Instruction: INP.
    *   Executing: Waiting for user input; Store user input in Accumulator: 20.

**Page 2**
*   **Instruction at Address 01 (STA num1):** (Blanks to be filled)
*   **Instruction at Address 02 (INP):** (Blanks to be filled)

**Page 3**
*   **Instruction at Address 03 (ADD num1):** (Blanks to be filled)
*   **Instruction at Address 04 (OUT):** (Blanks to be filled)
*   **Instruction at Address 05 (HLT):** (Blanks to be filled)

**Page 4**
*   **Reflection Questions:**
    1.  What happens during the fetch phase?
    2.  What is stored in the Accumulator after each instruction?
    3.  How does the Program Counter help in sequencing instructions?

---

### Part 2: Completed Exercise & Explanations

In this trace, we assume the first input was **20** (from the sample) and we will use **30** for the second input. In LMC (Little Man Computer) code: INP = 901, STA = 306, ADD = 106, OUT = 902, HLT = 000.

#### Page 2 Completion

**Instruction at Address 01 (STA num1)**
*   **Fetching Instruction...**
    *   Set MAR to value held by Program Counter: **1**
    *   Increment Program Counter by 1 → **2**
    *   Fetch instruction from address stored in MAR
    *   Fetched instruction: **306** stored in the MDR
    *   Copy instruction from the MDR to the CIR
*   **Decoding Instruction Stored in CIR...**
    *   Instruction: **STA 06**
*   **Executing Instruction...**
    *   Store value in Accumulator (**20**) into memory address (**06**)

**Instruction at Address 02 (INP)**
*   **Fetching Instruction...**
    *   Set MAR to value held by Program Counter: **2**
    *   Increment Program Counter by 1 → **3**
    *   Fetched instruction: **901** stored in the MDR
*   **Decoding Instruction Stored in CIR...**
    *   Instruction: **INP**
*   **Executing Instruction...**
    *   Waiting for user input
    *   Store user input in Accumulator: **30** (Assuming user inputs 30)

---

#### Page 3 Completion

**Instruction at Address 03 (ADD num1)**
*   **Fetching Instruction...**
    *   Set MAR to value held by Program Counter: **3**
    *   Increment Program Counter by 1 → **4**
    *   Fetched instruction: **106** stored in the MDR
*   **Decoding Instruction Stored in CIR...**
    *   Instruction: **ADD 06**
*   **Executing Instruction...**
    *   Add content of memory location **06** (which is 20) to Accumulator
    *   Accumulator now holds: **50** (30 + 20)

**Instruction at Address 04 (OUT)**
*   **Fetching Instruction...**
    *   Set MAR to value held by Program Counter: **4**
    *   Increment Program Counter by 1 → **5**
    *   Fetched instruction: **902** stored in the MDR
*   **Decoding Instruction Stored in CIR...**
    *   Instruction: **OUT**
*   **Executing Instruction...**
    *   Output value in Accumulator: **50**

**Instruction at Address 05 (HLT)**
*   **Fetching Instruction...**
    *   Set MAR to value held by Program Counter: **5**
    *   Increment Program Counter by 1 → **6**
    *   Fetched instruction: **000** stored in the MDR
*   **Decoding Instruction Stored in CIR...**
    *   Instruction: **HLT**
*   **Executing Instruction...**
    *   Program stops.

---

#### Page 4: Reflection Answers

1.  **What happens during the fetch phase?**
    *   **English:** The CPU gets the address of the next instruction from the Program Counter (PC) and copies it to the Memory Address Register (MAR). The instruction is then retrieved from memory, placed in the Memory Data Register (MDR), and copied to the Current Instruction Register (CIR). The PC is incremented.
    *   **Cantonese:** CPU 會從 PC 攞下一個指令嘅地址，放入 MAR。然後從記憶體讀取指令放入 MDR，再複製去 CIR。同時 PC 會加 1，準備下一條指令。

2.  **What is stored in the Accumulator after each instruction?**
    *   **English:** (00) 20; (01) 20; (02) 30; (03) 50; (04) 50; (05) 50.
    *   **Cantonese:** 隨住指令執行，ACC 數值分別係：輸入 20、保持 20、輸入 30、加完變 50、輸出 50、停機。

3.  **How does the Program Counter help in sequencing instructions?**
    *   **English:** It acts as a pointer that keeps track of the memory address for the next instruction to be executed, ensuring the program runs in the correct order.
    *   **Cantonese:** PC 係一個指針，記錄住下一條要執行指令嘅記憶體地址，確保個程式可以按正確順序運行。

---

### Detailed Explanation (English & Cantonese)

**1. Fetch Phase (擷取階段):**
*   **English:** The **Program Counter (PC)** tells the CPU where to look. We copy the PC value to the **MAR**. The instruction travels from RAM to the **MDR**, then finally to the **CIR** for the CPU to "read" it.
*   **Cantonese:** **PC (程序計數器)** 話畀 CPU 知下一條指令喺邊。我哋將 PC 嘅值抄去 **MAR (地址暫存器)**。指令會由 RAM 去到 **MDR (數據暫存器)**，最後去到 **CIR (當前指令暫存器)** 畀 CPU「睇」。

**2. Decode Phase (解碼階段):**
*   **English:** The Control Unit looks at the code in the **CIR** to understand what it needs to do (e.g., "STA" means store, "ADD" means plus).
*   **Cantonese:** 控制單元 (Control Unit) 會睇 **CIR** 入面嘅代碼，搞清楚要做啲咩（例如 "STA" 係儲存，"ADD" 係加法）。

**3. Execute Phase (執行階段):**
*   **English:** This is where the actual work happens. In **STA**, data moves from the **Accumulator (ACC)** to memory. In **ADD**, the ALU performs math.
*   **Cantonese:** 呢度係真正做嘢嘅階段。**STA** 嗰陣，數據會由 **ACC (累加器)** 搬去記憶體。**ADD** 嗰陣，運算單元 (ALU) 就會做加數。
