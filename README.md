Experimental environment: win10 x64    
Software official website:https://www.ejinshan.net/product_V9/index.html   
Software version:8.0.2389.45     
Affected Component: krecycle.exe   
 
The root cause of this vulnerability is that ordinary users can open the Falcon security software and construct a malicious sample.  
After being deleted by the Falcon security software, they can open the recovery area and restore the sample. However, when the Falcon security software restores the sample,  
if the sample was deleted originally If the directory does not exist, the user will specify any directory to restore. When restoring,     
it is not judged whether the restored directory has write permission for the current user. As a result, it can be restored     
to C:\Windows\System32 to achieve local privilege escalation.  
Before 19h1, any suffix file can be loaded by Diagnostics Hub Service to achieve local privilege escalation.    
Before 19h2, you can use the dui'xiang manager and directory link to create WindowsCoreDeviceInfo.dll. Finally, the Update Session Orchestrator service will execute     WindowsCoreDeviceInfo.dll  
