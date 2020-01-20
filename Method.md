## Tools & Resources

Free:  
* Policy Analyzer from Microsoft --> [Here](https://www.microsoft.com/en-us/download/details.aspx?id=55319)  
* 

Proprietary:  
* CIS --> [Here](https://www.cisecurity.org/cis-benchmarks/)


## Windows Policy Analysis

Note that the following is using CIS benchmarks which are proprietary.

### Policy Viewer Quick Overview

1. Export the Comp Table to Excel (Including Comp1, Comp2, LocalPolicies)
2. Go to the next free column (in my case H)
3. Apply the following formula where
    -F2 = comp2
    -E2 = comp1
    -D2 = local policy

```
=IF(AND(E2="";F2="");"";IF(D2<>"";IF(E2="";IF(F2="";"";IF(F2=D2;"MATCH";"MISMATCH"));IF(E2=D2;"MATCH";"MISMATCH"));""))
```

1. Export the User Table to Excel (Including User1, User2, LocalPolicies)
2. Go to the next free column (in my case H)
3. Apply the following formula where
    -F2 = User2
    -E2 = User1
    -D2 = local policy
```
=IF(AND(E2="";F2="");"";IF(D2<>"";IF(E2="";IF(F2="";"";IF(F2=D2;"MATCH";"MISMATCH"));IF(E2=D2;"MATCH";"MISMATCH"));""))
```

1. Export the User Table to Excel (Including User1, User2, LocalPolicies)
2. Go to the next free column (in my case H)
3. Apply the following formula where
    -F2 = Service2
    -E2 = Service1
    -D2 = local policy
```
=IF(AND(E2="";F2="");"";IF(D2<>"";IF(E2="";IF(F2="";"";IF(F2=D2;"MATCH";"MISMATCH"));IF(E2=D2;"MATCH";"MISMATCH"));""))
```
