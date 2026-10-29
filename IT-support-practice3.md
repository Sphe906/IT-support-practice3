# **Printer Troubleshooting — Windows Services and Diagnostics**

### **Problem Description**

A user reported that their printer would not print documents.

### **Investigation**

The following checks were performed to investigate the issue:

* Checked the Windows Print Spooler service.  
* Checked the available printers in Windows.  
* Tested printing using Microsoft Print to PDF.  
* Examined the PrintService Admin event log.  
* Inspected the Print Spooler dependencies.

### **Tools Used**

* Windows Services (`services.msc`)  
* Event Viewer (`eventvwr.msc`)  
* Command Prompt:  
  * `sc query spooler`  
  * `sc query RpcSs`  
  * `sc query HTTP`

### **Findings**

* **Print Spooler:** Running.  
* **RPC service:** Running.  
* **HTTP driver:** Running.  
* **Microsoft Print to PDF:** Successfully generated a PDF file.  
* **PrintService Admin log:** No events recorded.

### **Conclusion**

No evidence of a Windows printing subsystem failure was identified during the investigation.

Microsoft Print to PDF successfully processed a print job, demonstrating that virtual printing worked in the test environment.

However, a physical printer was not tested, so potential hardware, driver, connectivity, or device-specific problems could not be ruled out.

### **Outcome**

No configuration changes were made because the investigation did not identify a fault requiring correction.

### **Skills Practised**

* Windows service troubleshooting  
* Command-line diagnostics  
* Event Viewer investigation  
* Printer troubleshooting  
* Technical documentation

