# UiPath Flow Sequence – Repeat, While, and Do While Loops

This UiPath project demonstrates the use of **Repeat**, **While**, and **Do While** loops inside a Flow Sequence workflow.  
The example uses a simple integer variable `counter` to show how each loop behaves.

---

## 🎯 Project Objective

To understand how different loops work in UiPath:

| Loop Type | Executes At Least Once? | Condition Checked | Description |
|------------|--------------------------|------------------|--------------|
| **Repeat** | ✅ Yes (fixed count) | No condition | Runs a fixed number of times |
| **While**  | ❌ No | Before each iteration | Runs *while* a condition is true |
| **Do While** | ✅ Yes | After each iteration | Runs until a condition becomes false |

---

## 🧩 Variables

| Name | Type | Default Value | Description |
|------|------|----------------|--------------|
| `counter` | Int32 | 0 | Used to count and track loop iterations |

---

## ⚙️ Steps to Create in UiPath Studio

### 1. Create a New Project
- Open **UiPath Studio**
- Click **Process → New**
- Name it: `FlowSequenceLoops`
- Choose a folder and click **Create**

---

### 2. Add Variables
- Go to the **Variables** panel (bottom of the screen)
- Add:
  - `counter` → Type: **Int32**, Default: `0`

---

### 3. Build the Flow Sequence

#### 🧱 Step 1 – Assign
- Activity: **Assign**
- Expression:  
  `counter = 0`

---

#### 🔁 Step 2 – Repeat Number of Times
- Activity: **Repeat Number of Times**
- Property → `NumberOfTimes = 3`
- Inside Body:
  1. **Assign:** `counter = counter + 1`
  2. **Log Message:** `"Repeat Loop → Counter = " + counter.ToString`

---

#### 🔁 Step 3 – While Loop
- Activity: **While**
- Condition: `counter < 6`
- Inside Body:
  1. **Assign:** `counter = counter + 1`
  2. **Log Message:** `"While Loop → Counter = " + counter.ToString`

---

#### 🔁 Step 4 – Do While Loop
- Activity: **Do While**
- Condition: `counter < 9`
- Inside Body:
  1. **Assign:** `counter = counter + 1`
  2. **Log Message:** `"Do While Loop → Counter = " + counter.ToString`

---

#### ✅ Step 5 – Final Log Message
- Activity: **Log Message**
- Message: `"Final Counter = " + counter.ToString`

---

### OUTPUT  
<img width="1919" height="1018" alt="Screenshot 2025-11-11 082705" src="https://github.com/user-attachments/assets/044b965d-c26c-44c0-85a2-4c0a2d78ee0f" />


