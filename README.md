# Arduino-CoDeSys-NetVars
Arduino implementation to send and receive CoDeSys Network Variables (NetVars)

## Example

```
CoDeSysNetvars netvars("225.10.10.10", 1202, CoDeSysNetvars::TT_ONCHANGE);

setup:
netvars.clear();
netvars.add( CoDeSysNetvars::VT_REAL, "Temp1" );
netvars.add( CoDeSysNetvars::VT_REAL, "Temp2" );
netvars.add( CoDeSysNetvars::VT_REAL, "Temp3" );
netvars.add( CoDeSysNetvars::VT_REAL, "Temp4" );
netvars.begin();

loop:
netvars[0] = 10.0f;
netvars["Temp2"] = 20.0f;
netvars.handle();
```
