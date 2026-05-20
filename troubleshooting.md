## Car Raspberry Pi – Power Loss Behavior (Theoretical Design Consideration)

### **Context**
This project is currently in the planning phase. The following notes outline anticipated issues and solutions based on research and prior Pi experience.

### **Potential Problem**
A Raspberry Pi used as a car audio server would face abrupt power loss whenever the vehicle turns off.

### **Expected Symptoms**
- Filesystem corruption
- Slow boot times
- Service startup failures

### **Likely Root Cause**
Power being cut during write operations.

### **Planned Mitigation**
- Add a supercapacitor-based UPS module
- Use read-only filesystem optimizations
- Minimize background write operations

### **Expected Outcome**
A stable, resilient Pi that survives ignition power loss without corruption.
