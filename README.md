# Raw log
## Target N-TAS Event
    ⊙ HttpThreat
        - 2023-06-05T05:31:57.691
        - 18572
        - {145e89fa-a02a-64d1-ff6e-000000000f00}
        - C:\\Program Files (x86)\\ESTsoft\\ALPDF\\ALPDF.exe
    ⊙ DnsCovertChannel
        - 2023-06-05T05:28:57.594
        - 11220
        - {145e89fa-894a-64d1-066a-000000000f00}
        - C:\\Program Files (x86)\\G2BRUN\\g2brun.exe

## Target E-TAS Event
    ⊙ HttpThreat
        - networkConnection ✅
        - processCreate ✅
        - imageLoad ✅
        - fileCreate ✅
        - fileDelete ✅
        
    ⊙ dnsQuery
        - networkConnection ✅
        - dnsQuery ✅
        - processCreate ✅
        - imageLoad ✅
        - registryValueSet ✅

### Target E-TAS Candidate
    ⊙ networkConnection
        - Network
        - Event 3
    ⊙ dnsQuery
        - Network
        - Event 22
    ⊙ processCreate
        - Process
        - Event 1
    ⊙ imageLoad
        - File
        - Event 7
    ⊙ fileCreate
        - File
        - Event 11
    ⊙ registryValueSet
        - Registry
        - Event 13
    ⊙ fileDelete
        - File
        - Event 23
<br/><br/><br/>


# Detect log
## Goal
    A situation where both N-TAS and E-TAS detection events are detected on a single device over a specific period of time (approximately one month). Both N-TAS and E-TAS detection events are detected.
## Target
    ⊙ Datetime
        - 2023.07.01 ~ 2023.07.30 ✅
        - Random datetime ✅
    ⊙ Counts
        - 300 ✅
## Common spec
    ⊙ N-TAS
        - srcAddr : 41.179.253.229 ✅
    ⊙ E-TAS
        - agentName : DESKTOP-0FS3LG3 ✅
        - agentId : f98ce9dc-4df6-445a-890d-c7a5368c230d ✅
## N-TAS log
    ⊙ Target detect event
        - HttpThreat ✅
        - DnsCovertChannel ✅
## E-TAS log
    ⊙ Target detect event
        - Randsomware ✅
        - Rootkit ✅
        - Bootkit ✅


<br/>

#### Copyright 2023. ClumL Inc. all rights reserved