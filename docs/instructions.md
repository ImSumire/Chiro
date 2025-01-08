| Instruction | Description           | Operands | Pseudocode |
|-------------|-----------------------|----------|------------|
| `nop`       | No operation          |   |   |
| `halt`      | Halt (end of program) |   |   |
| `add`       | Addition              | `Target (Register)`, `Left (Literal/Register)`, `Right (Literal/Register)` | `Target = Left + Right` |
| `addi`      | Immediate addition    | `Target (Register)`, `Value (Literal/Register)` | `Target = Target + Value` |
| `sub`       | Subtraction           | `Target (Register)`, `Left (Literal/Register)`, `Right (Literal/Register)` | `Target = Left - Right` |
| `nor`       | Bitwise NOR           | `Target (Register)`, `Left (Literal/Register)`, `Right (Literal/Register)` | `Target = !(Left ∣ Right)` |
| `and`       | Bitwise AND           | `Target (Register)`, `Left (Literal/Register)`, `Right (Literal/Register)` | `Target = Left & Right` |
| `xor`       | Bitwise XOR           | `Target (Register)`, `Left (Literal/Register)`, `Right (Literal/Register)` | `Target = Left ^ Right` |
| `lshr`      | Right shift           | `Target (Register)`, `Value (Literal/Registeer)` | `Target = Value >> 1` |
| `goto`      | Jump                  | `Position (Label)` | `PC = Position` |
| `br`        | Conditional branch    | `Condition (Condition)`, `Position (Label)` | `PC = Condition ? Position : PC + 1` |
| `call`      | Function call         | `Position (Label)` | `PC = Position; Push (PC + 1) to Stack` |
| `return`    | Function return       |   | `PC = Top of Stack; Pop Stack` (Maybe have a return result) |
| `store`     | Memory Store          | `Target (Address/Register)`, `Value (Address/Literal/Register)` | `Target = Value` (Detects STR, LDI or LOD use) |
