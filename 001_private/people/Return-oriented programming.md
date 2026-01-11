#core/softwaredevelopment 

Return-oriented programming (ROP) is a powerful exploitation technique used to bypass modern security defenses like non-executable memory (DEP/NX) by **chaining together short instruction sequences (called gadgets) already present in a program’s memory.** Instead of injecting new code, attackers reuse existing code to execute arbitrary operations.

- **Definition:** ROP is a code-reuse attack where an attacker exploits a memory corruption vulnerability (e.g., buffer overflow) to hijack the program’s control flow and execute a series of small code fragments (*gadgets*), each ending with a `ret` instruction.
- **Purpose:** Allows execution of arbitrary code even when code injection is blocked by security mechanisms.

## How ROP Works

1. **Find a Vulnerability:** Attacker locates a memory corruption bug (like a stack buffer overflow).
2. **Control the Stack:** Overwrite return addresses on the stack to point to gadgets.
3. **Chain Gadgets:** Each gadget performs a small task; chaining them enables complex operations.
4. **Bypass Defences:** Since all code is already present and marked executable, ROP sidesteps protections like DEP/NX.

## Why ROP is Dangerous

- Bypasses non-executable memory protection.
- Enables arbitrary code execution without injecting new code.
- Generalises older attacks (e.g., return-to-libc) for more flexibility.

## ROP Attack Flow

1. Exploit stack vulnerability.
2. Overwrite return address with address of a gadget.
3. Stack is set up so each `ret` jumps to the next gadget.
4. Sequence of gadgets achieves the attacker's goal.

## Defences Against ROP

- **Control Flow Integrity (CFI):** Enforces valid control flow paths.
- **ASLR (Address Space Layout Randomisation):** Makes gadget addresses unpredictable.
- **Compiler-based mitigations:** Reduce usable gadgets or validate return addresses.


> [!info] **Key Takeaway**
> ROP is a technique that lets attackers execute arbitrary code by chaining existing code fragments, making it a major threat even in systems with modern memory protections.
