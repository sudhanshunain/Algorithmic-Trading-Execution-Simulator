# 🧠 Algorithmic Trading Strategies Simulator  
*A high-fidelity simulator for algorithmic execution strategies — starting with TWAP (Time-Weighted Average Price).*

---

## 👨‍💻 Author
**Sudhanshu Nain**  
*B.S. in Mathematics & Computing, IIT Patna*  
*Quantitative Research Intern — 26 Miles Capital (Quadeye Consultant)*  

---

## 💡 Project Background

During my summer internship at **26 Miles Capital**, I worked as a **Quantitative Researcher**, developing and testing algorithmic trading strategies for high-frequency environments.  

While my primary task was to **design and analyze trading strategies**, I developed a deep curiosity about **how orders are executed at the microstructure level** — particularly through **order books** and **execution algorithms**.  

This project, *Algorithmic Trading Strategies Simulator*, is a result of that curiosity.  
It simulates how a strategy like **TWAP (Time-Weighted Average Price)** executes large parent orders into smaller child orders under time and market constraints — a critical concept in execution algorithms.

---

## ⚙️ Implemented Strategy

### **TWAP (Time-Weighted Average Price)**  
TWAP slices a large order into equal parts that are executed evenly over a defined time period.  
This helps minimize **market impact**, **slippage**, and **information leakage**.

**Mathematical Definition:**  
\[
TWAP = \frac{\sum_i (Price_i \times TimeInterval_i)}{TotalTime}
\]

In this discrete-time simulator, orders are placed at uniform intervals.

---

## 📁 Project Structure

```bash
Algorithmic-Trading-Execution-Simulator/
├── CMakeLists.txt            # CMake build configuration
├── main.cpp                  # Simulation entry point
├── Order.hpp                 # Order data structure
├── OrderBook.hpp / .cpp      # Order book logic & logging
├── TWAPStrategy.hpp / .cpp   # TWAP algorithm implementation
└── ExecutionLog.csv          # Generated log of executed orders

## Build & Run (macOS)

### Prerequisites

- C++17 or newer
- CMake 3.15+
- Ninja or Make
- Xcode Command Line Tools (install using xcode-select --install)

# Clone the repository
git clone https://github.com/sudhanshu-nain/Algorithmic-Trading-Execution-Simulator.git
cd Algorithmic-Trading-Execution-Simulator

# Create build directory
mkdir -p build && cd build

# Configure and build
cmake .. -DCMAKE_BUILD_TYPE=Debug
cmake --build .

---

## Terminal Output
Executed order: ID=1 Price=100 Size=100
Executed order: ID=2 Price=100 Size=100
Executed order: ID=3 Price=100 Size=100
Executed order: ID=4 Price=100 Size=100
Executed order: ID=5 Price=100 Size=100
Executed order: ID=6 Price=100 Size=100
Executed order: ID=7 Price=100 Size=100
Executed order: ID=8 Price=100 Size=100
Executed order: ID=9 Price=100 Size=100
Executed order: ID=10 Price=100 Size=100
Execution complete. Log saved to ExecutionLog.csv

### Generated CSV Log
order_id,price,size
1,100,100
2,100,100
3,100,100
4,100,100
5,100,100
6,100,100
7,100,100
8,100,100
9,100,100
10,100,100