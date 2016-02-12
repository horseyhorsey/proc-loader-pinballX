### config with AHK
    [System_4]
    Name=P-ROC
    WorkingPath=C:\P-ROC\Visual Pinball
    Executable=vpinballx.exe
    LaunchBeforeWorkingPath=C:\P-ROC
    LaunchBeforeExecutable=PinXBefore.ahk
    Enabled=True
    TablePath=C:\P-ROC\Visual Pinball\Tables
    Parameters=-play "[TABLEPATH]\[TABLEFILE]"
    LaunchBeforeEnabled=True
    SystemType=1
    Bypass=True

### config with Exe
    [System_4]
    Name=P-ROC
    WorkingPath=C:\P-ROC\Visual Pinball
    Executable=vpinballx.exe
    LaunchBeforeWorkingPath=C:\P-ROC
    LaunchBeforeExecutable=PinXBefore.exe
    Enabled=True
    TablePath=C:\P-ROC\Visual Pinball\Tables
    Parameters=-play "[TABLEPATH]\[TABLEFILE]"
    LaunchBeforeEnabled=True
    SystemType=1
    Bypass=True
    